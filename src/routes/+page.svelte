<script>
    import "./root.scss";
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
