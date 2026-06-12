<script lang="ts">
    import favicon from "$lib/assets/favicon.svg";
    import "./splatoon-3-guide.scss";
    import tag from "$lib/assets/splatoon-3-guide/splashtag.png";
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <link
        rel="stylesheet"
        href="https://raw.githubusercontent.com/sindresorhus/modern-normalize/refs/heads/main/modern-normalize.css"
    />
</svelte:head>

<nav>
    <div><h2 style:color="yellow">/!\ under construction</h2></div>
    <div>
        <img
            src="https://media.tenor.com/9TsiJq--SsEAAAAj/doge-dance.gif"
            alt="doggo"
            style:width="100px"
            class="doggo"
        />
    </div>
    <div>
        <a href="https://haj-links.vercel.app" title="dd">
            <img src={tag} alt="tag" style:width="250px" /></a
        >
    </div>
</nav>

{@render children()}
