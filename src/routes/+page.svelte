<script>
    import lil_guy from "$lib/assets/ezgif.com-speed.png";
    function handleKeydown(event) {
        if (event.key == "p") {
            //goto("/room");
            window.location.href = "/room";
        }
    }
</script>

<svelte:window onkeydown={handleKeydown} />
<nav>
</nav>
<main>
    <div class="main_container">
    <img src={lil_guy} alt="lil guy" draggable="false"/>
    <div class="flex_vertical">
        <!--<h6>this website was made to practice css grid</h6>-->
<ul>
    <li>
    <a href="/graphicdesign">graphic designs</a></li>
    <li><a href="/portfolio">portfolio</a></li>
    <li><a href="/links">links</a></li>
    <li><a href="/splatoon-3-guide">"ability farming in splatoon 3"</a></li>
    <li><a href="/hatshell">hatshell font</a></li>
    <li><a href="/autum-leaf">autum leaf font</a></li>
</ul>
<h1>Hactuss</h1>
    </div>
    </div>
</main>
<footer>
    <div>
    <a href="https://github.com/hactuss">Github</a></div>
    <div>
    <a href="https://github.com/hactuss/hactuss-webpage">Website source</a></div>
</footer>
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

        width: 100%;
    }
    html {


    }
    body {
        width: 100%;
        background-color: hsl(0, 0%, 15%);
        color: white;
/*        display: flex;
        justify-content: center;
        align-items: center;*/
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
    ul, li{
        list-style: none;
    }
    img {

        width: 100%;
        aspect-ratio: 1/1;
        image-rendering: pixelated;
        vertical-align: middle;
        border: solid 1px white;
    }
    footer{
        background-color: hsl(0, 0, 25);
        bottom: 0;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content:flex-end;
    }
}
.main_container{
    display: flex;
}
.flex_vertical{
    display: flex;
    flex-direction: column;
}
</style>
