<script lang="ts">
    import favicon from "$lib/assets/favicon.svg";
    import tag from "$lib/assets/splatoon-3-guide/splashtag.png";
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
</svelte:head>
<!-- --
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
-->

{@render children()}
<style>
    :global{
    :root {
        --margin: 3rem;
        --small-margin: 1rem;
        --doggo-margin: 5%;
        --light-color: rgb(175 175 175);

        font-family: Arial, Helvetica, sans-serif;
        background-color: black;
        color: var(--light-color);
    }

    a {
        color: rgb(00 250 150);
    }

    td {
        border: solid var(--light-color) 1px;
        background-color: rgba(33 33 33);
    }
    thead {
        background-color: rgb(44 44 44);
    }
    table {
        width: 75%;
    }

    nav {
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    body {
        margin-left: var(--margin);
        margin-right: var(--margin);
    }

    @media screen and (width <= 600px) {
        body {
            margin-left: var(--small-margin);
            margin-right: var(--small-margin);
        }
        table {
            width: 100%;
        }
    }

    .doggo {
        animation-name: spin;
        animation-duration: 3000ms;
        animation-iteration-count: infinite;
        animation-timing-function: linear;

        margin-left: var(--doggo-margin);
        margin-right: var(--doggo-margin);
    }
    @keyframes spin {
        from {
            transform: rotate(0deg);
        }

        to {
            transform: rotate(360deg);
        }
    }
}
</style>
