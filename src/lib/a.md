There are a few good approaches, depending on how often the descriptions change.

### Option 1: Store the descriptions in an array (recommended)

Instead of relying on the filename, define your images and descriptions together.

```ts
// gallery.ts
const importedImages = import.meta.glob(
  '/src/lib/images/*.{jpg,png,webp}',
  {
    eager: true,
    import: 'default'
  }
);

export const gallery = [
  {
    src: importedImages['/src/lib/images/cat.jpg'],
    title: 'Cat',
    description: 'A sleepy orange cat.'
  },
  {
    src: importedImages['/src/lib/images/dog.jpg'],
    title: 'Dog',
    description: 'A happy golden retriever.'
  }
];
```

Then in your Svelte component:

```svelte
<script lang="ts">
  import { gallery } from '$lib/gallery';
</script>

{#each gallery as image}
  <figure>
    <img src={image.src} alt={image.title} />
    <figcaption>
      <h3>{image.title}</h3>
      <p>{image.description}</p>
    </figcaption>
  </figure>
{/each}
```

This is the cleanest solution because all the metadata lives with the images.

---

### Option 2: Match descriptions by filename

If you already have lots of images, you can keep a separate lookup object.

```ts
const images = import.meta.glob(
  '/src/lib/images/*.{jpg,png}',
  {
    eager: true,
    import: 'default'
  }
);

const descriptions: Record<string, string> = {
  'cat.jpg': 'A sleepy orange cat.',
  'dog.jpg': 'A happy golden retriever.'
};

const gallery = Object.entries(images).map(([path, src]) => ({
  src,
  filename: path.split('/').pop()!,
  description: descriptions[path.split('/').pop()!] ?? 'No description.'
}));
```

---

### Option 3: Use a JSON file (great for many images)

**gallery.json**

```json
[
  {
    "file": "cat.jpg",
    "title": "Cat",
    "description": "A sleepy orange cat."
  },
  {
    "file": "dog.jpg",
    "title": "Dog",
    "description": "A happy golden retriever."
  }
]
```

Then combine it with the imported images:

```ts
import metadata from './gallery.json';

const images = import.meta.glob(
  '/src/lib/images/*.{jpg,png}',
  {
    eager: true,
    import: 'default'
  }
);

const gallery = metadata.map((item) => ({
  ...item,
  src: images[`/src/lib/images/${item.file}`]
}));
```

This scales well if you have dozens or hundreds of images.

### Which should you choose?

* **A handful of images:** Option 1 is simple and readable.
* **Lots of images with metadata:** Option 3 (JSON) is the most maintainable.
* **Descriptions generated elsewhere (CMS, database):** Fetch the metadata from the backend and combine it with the image URLs.

For a portfolio or gallery in SvelteKit, the JSON approach is often the easiest to maintain as the project grows.
