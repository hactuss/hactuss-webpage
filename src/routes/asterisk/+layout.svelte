<script lang="ts">
    import favicon from "$lib/assets/asterisk/favicon.svg";
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <title>hactuss | asterisk design</title>
</svelte:head>
{@render children()}
