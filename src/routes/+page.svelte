<script>
    import lil_guy from "$lib/assets/ezgif.com-speed.png";
    import Device from 'svelte-device-info';
    function handleKeydown(event) {
        if (event.key == "p") {
            //goto("/room");
            window.location.href = "/room";
        }
    }
</script>

<svelte:window onkeydown={handleKeydown} />
{#if Device.isPhone == true}
<meta http-equiv="refresh" content="0; url=/m">
{/if}
<main>
    <div class="main_container">
        <div class="image_container">
            <div class="subcontainer">
            <img src={lil_guy} alt="lil guy" draggable="false"/>
            <p>Keep pushing!</p>
            </div>
        </div>
        <div class="flex-vertical text-center place-content-center all-the-text">
            <!--<h6>this website was made to practice css grid</h6>-->
            <h1>Hactuss</h1>
            <ul class="text-list">
                <li><a href="https://github.com/hactuss">Github</a></li>
                <li><a href="https://youtube.com/@hactuss">Youtube</a></li>
                <!--<li><a href="/graphicdesign">graphic designs</a></li>-->
                <li><a href="/portfolio">portfolio</a></li>
                <li><a href="/links">links</a></li>
                <li><a href="/splatoon-3-guide">"ability farming in splatoon 3"</a></li>
                <!--<li><a href="/hatshell">hatshell font</a></li>-->
                <!--<li><a href="/autum-leaf">autum leaf font</a></li>-->
                <li><a href="https://isitspookymonth.vercel.app">is it spooky month</a></li>
            </ul>
        </div>
    </div>
</main>

<style lang="scss">
/*@import "tailwindcss";*/
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
        transition-duration: 0.2s;
        transition-timing-function: ease-in-out;
        /*border: solid 1px red;*/
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
        height: 100dvh;
        display: flex;
        justify-content: center;
    }
    h1 {
        letter-spacing: -1px;
    }
    a {
        margin-bottom: 200px;
        color: hsl(200, 75%, 75%);
        text-decoration: none;
        /*&:hover {
            color: hsl(200, 75%, 85%);

        }*/
    }
    ul, li{
        list-style: none;
    }
    img {
        width: auto;
        aspect-ratio: 1/1;
        image-rendering: pixelated;
        vertical-align: middle;
        border: solid 1px white;
        /*&:hover{
            transform: scale(1.1);
        }*/
    }
    .subcontainer{
        transition-duration: 0.3s;
        transition-timing-function: ease;
        > p {
            opacity: 0;
            transition-duration: 0.3s;
            transition-timing-function: ease;
        }
        &:hover{
            transform: scale(1.1);
            > p{
                opacity: 0.3;
            }
        }
    }
    .image_container{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        text-align: center;
    }
    footer{
        background-color: rgab(11, 11, 11, 1);
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
/*
.flex_vertical{
    display: flex;
    flex-direction: column;
    }*/
.all-the-text{
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    > ul{
        &:hover{
        /*background-color: rgba(0, 0, 0, 0.2);*/
        color:hsla(200, 75%, 75%, 0.3);
        > li > a{opacity: 0.4;}
        }
    }
    > ul > li > a{
        &:hover{
            opacity: 1;
            color:  hsl(200, 75%, 75%);
        }
    }
}


/*ul > li > a:hover{

    color:hsla(200, 75%, 75%, 0.3);
}

.all-the-text > ul > li > a:hover{
color: hsl(200, 75%, 75%);
}*/
@media (m < 13){

}
</style>
