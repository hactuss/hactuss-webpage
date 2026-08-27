<script>
    import ng from "$lib/assets/ng_logo.png";
    let content = $state("default");
    let story = $state("blablabla");
    let story_cr = "creative stuff I do";
    let story_pr = "productive stuff I do";
    let story_ft = "free time stuff I do";
    let story_st = "state stuff I do";

    function setDefault() {
        content = "default";
        story = "blablabla";
    }

    // for testing
    let mobileinfo = $derived(true);
    let scrollText1 = $state("71");
    let scrollText2 = $state("72");
</script>

<!-- --
{#if (mobileinfo = true)}
    <div class="mobileinfo">
        <div class="mobileinfobox">
            <h2>Info</h2>
            <p>
                The device you are currently using is not supported by my
                website. Howerver, I wont stop you from trying to.
            </p>
            <h6>- hactuss</h6>
            <button
                onclick={() => {
                    console.log("pressed");
                    mobileinfo = false;
                }}>proceed at the risk of the site looking like trash</button
            >
        </div>
    </div>
{/if}
-->
<main data-theme="dark">
    <header>
        <img
            src="https://media1.tenor.com/m/mc3OyxhLazUAAAAC/doggo-doge.gif"
            alt="doggo"
            class="doggo"
        />

        <div>
            <p>
                Hello, my [psydonym/alias] is Hactuss. I make art, websites and
                videos sometimes. You can find most of my socials <a
                    href="https://haj-links.vercel.app/"
                    target="_blank">HERE.</a
                >
            </p>
            <p>
                This site is basically a bigger version of the hobby discription
                from my <a
                    href="https://hactuss-portfolio.vercel.app/"
                    target="_blank">PORTFOLIO.</a
                >
            </p>
        </div>
    </header>
    {#if false}
        <div style:display="flex">
            <img src={ng} alt="ng" width="250em" />
            <h1>ART</h1>
            <p>I post my art on ng</p>
        </div>

        <div class="grid">
            <div
                class="col"
                onmouseenter={() => {
                    content = "creative";
                    story = story_cr;
                }}
                onmouseleave={() => {
                    setDefault();
                }}
            >
                <h4>creative</h4>
                <div class="cr">
                    <ul>
                        <li>art (ng)</li>
                        <li>video editing (yt)</li>
                    </ul>
                </div>
            </div>
            <div
                class="col"
                onmouseenter={() => {
                    content = "productive";
                    story = story_pr;
                }}
                onmouseleave={() => {
                    setDefault();
                }}
            >
                <h4>productive</h4>
                <div class="pr">
                    <ul>
                        <li>personal organization (obsidian)</li>
                        <li>office</li>
                        <li>ability farming</li>
                    </ul>
                </div>
            </div>
            <div
                class="col"
                onmouseenter={() => {
                    content = "free time";
                    story = story_ft;
                }}
                onmouseleave={() => {
                    setDefault();
                }}
            >
                <h4>free time</h4>
                <div class="ft">
                    <ul>
                        <li>linux rice</li>
                        <li>splatoon</li>
                        <li>boredom</li>
                    </ul>
                </div>
            </div>
            <div
                class="col"
                onmouseenter={() => {
                    content = "state";
                    story = story_st;
                }}
                onmouseleave={() => {
                    setDefault();
                }}
            >
                <h4>state</h4>
                <div class="st">
                    <ul>
                        <li>future</li>
                        <li>selfhosting</li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="topic-content">
            <h2>{content}</h2>
            <p>{story}</p>
        </div>
        <div>
            <h1>moving text</h1>
            <div style:overflow="hidden">
                <p class="marquee">
                    <span>1 2 3 4 5 6 7 8 9 0</span>
                </p>
                <p class="marquee2">
                    <span>&#160 1 2 3 4 5 6 7 8 9</span>
                </p>
            </div>
        </div>
        <div class="stc">
            <p class="st one">{scrollText1}</p>
            <p class="st two">{scrollText2}</p>
        </div>
    {/if}
</main>

<style lang="scss">
    :global{
        /*
        https://www.dafont.com/de/monogramos.font
        https://www.dafont.com/de/diamondgrams.font
        */
        :root {
            font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
            font-family:
                "Circular Bold", "Helvetica Neue", Helvetica, Arial, sans-serif;
            font-size: 1.5rem;
        }
        * {
            margin: 0;
            padding: 0;
            border: 0;
        }
        /* ------------------------------------------------------------ */
        html {
            background-color: rgb(240, 240, 240);
            background-color: black;
            /*
            cursor:
                url("./lib/assets/Cursor.cur") 2 2,
                auto;
            */
        }
        body {
            color: blue;
            accent-color: blue;
            //padding-inline: 12.5%;
        }
        main[data-theme="light"] {
            background-color: white;
        }

        main[data-theme="dark"] {
            background-color: rgb($tone, $tone, $tone);
            color: white;
        }

        /* ------------------------------------------------------------ */

        header {
            display: flex;
            flex-direction: row;
            align-items: center;
        }
        nav {
            background: #ffb4b4;
            background: linear-gradient(
                0deg,
                rgba(255, 180, 180, 1) 0%,
                rgba(255, 255, 255, 1) 20%
            );
            color: black;
        }
        .nav {
            font-size: 0.5rem;

            display: flex;
            justify-content: space-between;
            align-items: center;
            text-align: center;
            margin-inline: 1%;
        }
        h1 {
            height: 100%;
            text-align: center;
            align-self: center;

            font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        }
        h4 {
            justify-self: center;
        }
        p {
            font-size: 1rem;
        }
        a {
            text-decoration: none;
        }
        a:hover {
            color: rgb(255 20 10);
        }
        img {
            image-rendering: pixelated;
        }
        svg {
            color: black;
            width: 1.5rem;
        }
        ul {
            text-decoration: none;
            list-style: none;
        }
        button {
            padding: 1px;
            border-radius: 2px;
        }
        button:active {
            background-color: red;
        }

    }
    .marquee {
        margin: 0 auto;
        white-space: nowrap;
        overflow: hidden;

        border: solid red 1px;
        width: 100%;
    }

    .marquee span {
        display: inline-flex;
        padding-left: 100%;
        animation: marquee 10s linear infinite;
    }
    .marquee2 {
        margin: 0 auto;
        white-space: nowrap;
        overflow: hidden;
        border: solid red 1px;
        width: 100%;
    }
    .marquee2 span {
        display: inline-flex;
        padding-left: 100%;
        animation: marquee 10s linear infinite;
    }
    @keyframes marquee {
        0% {
            transform: translate(0, 0);
        }
        100% {
            transform: translate(-100%, 0);
        }
    }
    @keyframes marquee2 {
        0% {
            transform: translate(0, 0);
        }
        100% {
            transform: translate(-100%, 0);
        }
    }
    /*{
        animation: scrolling-text 1s linear infinite;
    }*/
    .stc {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-shrink: 0;
        overflow-y: hidden;
    }
    .one {
        position: absolute;
        animation: flex-one 3s infinite linear;
        width: 100px;
    }
    .two {
        position: absolute;
        animation: flex-two 3s infinite linear;
        width: 100px;
    }

    @keyframes flex-one {
        from {
            transform: translate(0, 0);
        }
        to {
            transform: translate(-100%, 0);
        }
    }
    @keyframes flex-two {
        from {
            transform: translate(0, 0);
        }
        to {
            transform: translate(-100%, 0);
        }
    }
    @keyframes scrolling-text {
        from {
            transform: translateX(00%);
        }
        to {
            transform: translateX(-100%);
        }
    }

    :root {
        --cr-color: rgba(255, 0, 0, 0.5);
        --pr-color: rgba(255, 0, 0, 0.5);
        --ft-color: rgba(255, 0, 0, 0.5);
        --st-color: rgba(255, 0, 0, 0.5);
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: repeat(4, 1fr);

        grid-template-areas: "";
        column-gap: 2%;
        margin: 1%;
    }
    /*
    .grid {
        column-count: 4;
    }*/

    .col {
        width: 100%;
    }
    .cr {
        border: solid;
        border-image: linear-gradient(var(--cr-color), rgba(0, 0, 0, 0)) 1;
    }
    .pr {
        border: solid;
        border-image: linear-gradient(var(--pr-color), rgba(0, 0, 0, 0)) 1;
    }
    .ft {
        border: solid;
        border-image: linear-gradient(var(--ft-color), rgba(0, 0, 0, 0)) 1;
    }
    .st {
        border: solid;
        border-image: linear-gradient(var(--st-color), rgba(0, 0, 0, 0)) 1;
    }
    .flex {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
    }
    .mobileinfo {
        position: absolute;
        inset: 0 0 0 0;
        background-color: rgba(0, 0, 0, 0.7);
    }
    .mobileinfobox {
        background-color: rgba(33, 33, 33, 1);
        border: solid black 5%;
        border-radius: 10px;
        margin: 5%;
        padding: 2%;
    }
    .doggo {
        width: 10%;
        height: 10%;
        margin-right: 1rem;
    }
</style>
