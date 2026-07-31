<script lang="ts">
    import favicon from "$lib/assets/favicon/fav_big_blue_whitebg.svg";
    let { children } = $props();
</script>

<svelte:head>
    <title>hactuss - graphic designer and webdev</title>
<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
