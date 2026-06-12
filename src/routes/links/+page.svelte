<script>
    import { onMount } from "svelte";
    import "./links.scss";

    let NUMBER_EQUALS_CHARACTERS = 6;
    let EQUAL_CHARACTERS = "=".repeat(250);
    let EQUAL_CHARACTERS_side = "=".repeat(250);

    let cursor = $state(" ");
    onMount(() => {
        const interval = setInterval(() => {
            if (cursor == " ") {
                cursor = "_";
            } else {
                cursor = " ";
            }
        }, 500);

        return () => {
            clearInterval(interval);
        };
    });

    let MAIN_WIDTH = 0;
    let MAIN_MIN_WIDTH = 1700;
    let PORTFOLIO_TEXT = ">> my portfolio <<";
    function setAmountofEqualCharacters() {
        EQUAL_CHARACTERS.repeat(+1);
        return console.log(NUMBER_EQUALS_CHARACTERS);
    }
    //console.log(visualViewport?.width + "x" + visualViewport?.height);
    console.log("https://haj-links.vercel.app/signs");
</script>

<!--
<p>Actual width: {MAIN_WIDTH}</p>
<p>Min width: {MAIN_MIN_WIDTH}</p> -->

<div class="newblock">
    <p class="border">{EQUAL_CHARACTERS}</p>
    <div class="flex-r">
        <div class="border-left border">{EQUAL_CHARACTERS_side}</div>
        <div class="nb-inner">
            <h1>Hactuss{cursor}</h1>
            <div class="doggo-container">
                <img
                    src="https://media.tenor.com/9TsiJq--SsEAAAAj/doge-dance.gif"
                    alt="doggo"
                    class="doggo"
                />
            </div>
            <a href="https://github.com/hactuss">Github</a>
            <a href="https://hactuss.vercel.app">Homepage</a>
            <a href="https://hactuss.newgrounds.com">Newgrounds</a>
            <a href="https://youtube.com/@hactuss">YouTube</a>

            <h2>
                <a href="https://hactuss-portfolio.vercel.app/"
                    >{PORTFOLIO_TEXT}</a
                >
            </h2>
            <br />
            <h2>
                Projects that are <a
                    href="https://www.youtube.com/watch?v=bJQj1uKtnus"
                    class="done"
                    target="_blank">done</a
                >
            </h2>
            <a href="https://isitspookymonth.vercel.app">is it spooky month?</a>
            <a href="https://officehaj.vercel.app">The office</a>
            <a href="https://center-calc.vercel.app">center calculator</a>
            <a href="https://ability-farming.vercel.app/"
                >ability farming guide for Splatoon 3 players</a
            >
        </div>
        <div class="border-right border">{EQUAL_CHARACTERS_side}</div>
    </div>
    <p class="border-bottom border">{EQUAL_CHARACTERS}</p>
</div>

<!-- ▎▒-->
<style>
    * {
        margin: 0%;
        padding: 0;
        border: 0;
    }
    a {
        margin-top: 1rem;
        margin-bottom: 1rem;
        background-color: rgba(255, 255, 255, 0.1);
        display: block;
    }
    .flex-r {
        display: flex;
        flex-direction: row;
        overflow: hidden;
    }
    .newblock,
    .border-left {
        overflow: hidden;
        height: 100dvh;
    }
    .border-bottom {
        position: fixed;
        bottom: 0;
    }
    .nb-inner {
        /*border: solid blueviolet 1px;*/
        width: 100%;
    }
    .border-left,
    .border-right {
        writing-mode: sideways-lr;
    }
    .done {
        display: inline;
        background-color: rgba(0, 0, 0, 0);
        text-decoration: none;
    }
    .doggo {
        animation-name: spin;
        animation-duration: 3000ms;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
        margin-top: 3%;
        margin-bottom: 3%;
    }
    .doggo-container {
        background-color: rgba(255, 255, 255, 0.1);
    }
    @keyframes spin {
        from {
            transform: rotate(0deg);
        }

        to {
            transform: rotate(360deg);
        }
    }
</style>
