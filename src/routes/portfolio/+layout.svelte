<script lang="ts">
    import favicon from "$lib/assets/portfolio/images/favicon.svg";
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <title>Hactuss Portfolio</title>
</svelte:head>

{@render children?.()}
