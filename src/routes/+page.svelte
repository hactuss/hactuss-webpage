<script>
    import pixel from "$lib/assets/pixel.png";
    import lil_guy from "$lib/assets/ezgif.com-speed.png";
    function handleKeydown(event) {
        if (event.key == "p") {
            //goto("/room");
            window.location.href = "/room";
        }
    }
</script>

<svelte:window onkeydown={handleKeydown} />
<main>
    <img src={lil_guy} alt="lil guy" draggable="false"/>
    <br />
    <a href="/graphicdesign">graphic designs</a>
    <a href="/portfolio">portfolio</a>
    <a href="/links">links</a>
    <a href="/splatoon-3-guide">"ability farming in splatoon 3"</a>
    <a href="/hatshell">hatshell font</a>
    <a href="/autum-leaf">autum leaf font</a>
</main>
<style lang="scss">
    :global{
    :root {
        font-family: monospace;
        font-size: 1.5rem;
    }
    * {
        margin: 0;
        padding: 0;
        font-size: clamp (1em, 1em, 1em);
    }
    html {
        overflow: hidden;
        width: 100%;
    }
    body {
        height: 90dvh;
        width: 100%;
        background-color: hsl(0, 0%, 15%);
        color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    main {
        width: 100%;
    }
    h1 {
        letter-spacing: -1px;
    }
    a {
        margin-bottom: 200px;
        color: hsl(200, 75%, 75%);
        &:hover {
            color: hsl(200, 75%, 85%);
            text-decoration: none;
        }
    }
    img {
        width: clamp(40%, 20%, 10%);
        aspect-ratio: 1/1;
        image-rendering: pixelated;
        vertical-align: middle;
    }
}
</style>
