<script lang="ts">
    import favicon from "$lib/assets/asterisk/favicon.svg";
    import "./asterisk.scss";
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <title>hactuss | asterisk design</title>
</svelte:head>
{@render children()}
