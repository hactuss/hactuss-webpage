<script>
    import "./graphicdesign.scss";
    const imageModules = import.meta.glob("$lib/assets/graphicdesign/*", {
        query: "?url",
    });
    const images = Object.entries(imageModules).map(([url]) => ({ url }));
</script>

<main>
    <header>
        <h1>Hactus Design - this site is unproportional</h1>
    </header>
    <main>
        <div class="gallery">
            {#each images as image}
                <img src={image.url} alt={image.url} />
            {/each}
        </div>
    </main>
</main>

<style>
    main {
        width: 100vw;
    }
    .gallery {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>
