<script lang="ts">
    import favicon from "$lib/assets/links/doggo.gif";
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <link
        rel="stylesheet"
        href="https://raw.githubusercontent.com/sindresorhus/modern-normalize/refs/heads/main/modern-normalize.css"
    />
    <title>hactuss linktree</title>
</svelte:head>

{@render children?.()}
