<script lang="ts">
    import ProjectCard from "$lib/components/ProjectCard.svelte";
    import ghlogo from "$lib/assets/portfolio/images/github-mark-white.svg";
    let cursor = $state("_");
    function blink() {
        if (cursor == "_") {
            cursor = " ";
        } else {
            cursor = "_";
        }
    }
</script>

<!--
<pre>
 ___  ___  ________  ________ _________  ___  ___  ________   ________
|\  \|\  \|\   __  \|\   ____\\___   ___\\  \|\  \|\   ____\ |\   ____\
 \ \  \\\  \ \  \|\  \ \  \___\|___ \  \_\ \  \\\  \ \  \___|_\ \  \___|_
  \ \   __  \ \   __  \ \  \       \ \  \ \ \  \\\  \ \_____  \\ \_____  \
   \ \  \ \  \ \  \ \  \ \  \____   \ \  \ \ \  \\\  \|____|\  \\|____|\  \
    \ \__\ \__\ \__\ \__\ \_______\  \ \__\ \ \_______\____\_\  \ ____\_\  \
     \|__|\|__|\|__|\|__|\|_______|   \|__|  \|_______|\_________\\_________\
                                                      \|_________\|_________|
</pre> -->

<main id="MAIN_CONTAINER">
    <main id="SIDEBAR">
        <span id="SIDEBAR_TEXT">H A C T U S S</span>
        <div id="gh_link" class="marked">
            <a href="https://github.com/hactuss" id="githublogo" class="marked">
                <img src={ghlogo} alt="github_logo" class="marked" />
            </a>
        </div>
    </main>
    <main id="MAIN_CONTENTS">
        <header>
            <div class="header-1">
                <div class="name-text">
                    <h1>Name: <span id="marked1">Hactuss</span></h1>
                    <p></p>
                </div>
                <ul>
                    <li>Frontend webdevelopment as a hobby</li>
                    <li>
                        Primary programming language: <a
                            id="marked2"
                            class="marked"
                            href="https://svelte.dev/">Svelte</a
                        ><!-- --
            and
            <a id="marked3" href="https://sass-lang.com/">SCSS</a>-->
                    </li>
                    <!-- --
          <li>
            Currently learning <a id="marked5" href="https://rust-lang.org">
              Rust
            </a>
          </li>-->
                </ul>
            </div>
            <!-- --
      <div class="header-2" style:border="1px solid white">
        <h2>second box</h2>
        </div>-->
        </header>
        <hr />
        <div id="Projects_wrapper">
            <h2>Projects</h2>
            <ProjectCard
                title="Portfolio"
                buildtime="Nov 2. 2025"
                discription="This portfolio I created to tell about my projects and work."
                url="/"
                url_gh="https://github.com/hactuss/portfolio"
            />
            <ProjectCard
                title="Center Calculator"
                buildtime="Sep 27. 2025"
                discription="A web app to automate the process of calculating the center of a given area. Useful in graphic design and more."
                url="https://center-calc.vercel.app"
                url_gh="https://github.com/hactuss/ccenter"
            />
            <ProjectCard
                title="Worldclock"
                buildtime="Dec 31. 2023"
                discription="a website to show the current time in different timezones. Useful when interacting with people from all around the world. (Currently being rewritten in svelte.)"
                url="https://hactuss.github.io/pages/office/office.html"
                url_gh="https://github.com/hactuss/hactuss.github.io"
            />
            <ProjectCard
                title="The office"
                buildtime="Aug 12. 2025"
                discription="a website for various timezones written in svelte"
                url="https://officehaj.vercel.app/"
                url_gh="https://github.com/hactuss/office-haj"
            />
            <ProjectCard
                title="It is spooky month?"
                buildtime="Sep 15. 2025"
                discription="a small jokewebsite I built in reference to the Spooky Month indie animation series. Shows something special in october."
                url="https://isitspookymonth.vercel.app"
                url_gh="https://github.com/hactuss/isitspookymonthdotcom"
            />
            <!--
      <ProjectCard
        title="Ultrakill Terminal"
        buildtime="Nov 29. 2025"
        discription="a recreation of the terminals from the indiegame 'Ultrakill'"
        url="https://uk-terminal.vercel.app"
        url_gh="https://github.com/hactuss/uk-terminal"
      />
      <ProjectCard
        title="Aero Calendar"
        buildtime="Dec 9. 2025"
        discription="A simple yet funcional calendar in the Aero style"
        url="https://aerocalendar.vercel.app"
        url_gh="https://github.com/hactuss/aerocalendar"
      />-->
        </div>
        <hr />
        <div>
            <h2>Personality</h2>
            <div>
                <h3>Hobbies</h3>
                <ul>
                    <li>Videoediting</li>
                    <li>
                        Experimenting with Linux (Specifically <a
                            id="marked4"
                            class="marked"
                            href="https://nixos.org/">NixOS</a
                        >)
                    </li>
                    <li>Drawing comics</li>
                    <li>
                        Reading books regarding my hobbies or general literature
                    </li>
                    <li>Gaming (Splatoon 3)</li>
                </ul>
            </div>
        </div>
        <hr />
        <footer>
            <p>
                Contact me via Email: <a
                    href="mailto:hactuss@proton.me"
                    class="marked"
                    ><span id="marked1" class="marked">hactuss@proton.me</span
                    ></a
                >
            </p>
        </footer>
    </main>
</main>

<style>
    :global {
    * {
        margin: 5px;
        /*font-family: "DugasPro";*/
        color: hsl(0 0 80%);
        cursor: url("$lib/assets/portfolio/images/Cursor.png"), auto;
    }
    :root {
        font-size: 1.25rem;
        white-space: collapse;
        font-family: monospace;
        --white: color: hsl(0 0 79);
    }
    @font-face {
        font-family: "DugasPro";
        src:
            local("DugasPro"),
            url("./lib/assets/fonts/dugas_pro/ttf/DugasPro-RegularCondensed.ttf");
    }
    * {
        ::selection {
            color: rgb(50 50 50);
            background-color: rgb(200 250 20);
        }
    }

    :global(html) {
        background-color: rgb(30 30 30);
        background-image: url("https://imgs.search.brave.com/bDx7OquS6IrpfGWWKAKuLEB978SrEmZYS_wT76gkmLg/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly93YWxs/cGFwZXJzLmNvbS9p/bWFnZXMvZmVhdHVy/ZWQvY29uY3JldGUt/dGV4dHVyZS1waWN0/dXJlcy1yZzF5aGRo/dTlrYnVpbmZ3Lmpw/Zw");
        background-size: contain;
        background-image: none;
        cursor:
            url("../../lib/assets/images/Cursor.cur") 0 0,
            default;
    }
    a,
    img {
        cursor:
            url("$lib/assets/images/Clicker.cur") 0 0,
            pointer;
    }
    header {
        display: flex;
    }
    footer {
        font-size: 0.8rem;
    }
    :global(
    li,
    ul) {
        list-style-type: "▷ ";
        list-style-type: "◦ ";
        list-style-type: "》";
        list-style-type: "> ";
        list-style-type: "⁎ ";

        /*
      https://www.madeintext.com/gaming-symbols/
      https://www.madeintext.com/minecraft-symbols/
      https://www.madeintext.com/star-symbols/
      https://www.madeintext.com/circle-symbols/
      */
    }
a {
        color: #c8fa14;
    }
    hr {
        width: 110%;
    }
}
    #SIDEBAR {
        flex: 1;
        display: flex;
        flex-direction: column;
        align-items: center;
        /*background-color: rgb(50, 50, 50);*/
        background: #0a0a0a;
        background: linear-gradient(
            90deg,
            rgba(10, 10, 10, 1) 5%,
            rgba(50, 50, 50, 1) 50%,
            rgba(100, 100, 100, 1) 75%,
            rgba(200, 200, 200, 1) 90%,
            rgba(125, 125, 125, 1) 100%
        );
    }
    #SIDEBAR_TEXT {
        writing-mode: vertical-lr;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    #MAIN_CONTAINER {
        margin-left: 12.6%;
        margin-right: 12.6%;
        display: flex;
        flex-direction: row;
        height: 100%;
        backdrop-filter: brightness(0);

        filter: brightness(1);
    }
    #MAIN_CONTENTS {
        display: flex;
        flex-direction: column;
        overflow: hidden;
        justify-content: center;
    }

    .header-1 {
        width: 100%;
    }
    /*
    #SIDEBAR_LOGO {
        background-color: rgb(50 50 50);
        width: fit-content;
        height: fit-content;
        padding: 10px;
        border: transparent solid 1px;
        border-radius: 5px;
    }
    #SCREENSHOT_DISPLAY {
        opacity: 0.75;
        width: 400px;
    }
    #Projects_wrapper {
        border: solid 1px white;
    }*/
    img {
        width: 2.25rem;
    }
    span {
        margin: 0;
        padding: 0;
    }

    #marked1 {
        color: rgb(200 250 20);
    }
    #marked2 {
        color: rgb(234 80 39);
    }
    /*#marked3 {
        color: rgb(193 106 152);
    }*/
    #marked4 {
        color: rgb(82 107 171);
    }
    /*#marked5 {
        color: rgb(140 87 53);
    }*/
    .marked {
        cursor:
            url("$lib/assets/portfolio/images/Clicker.cur") 0 0,
            pointer;
    }
    @media screen and (width <= 500px) {
        #MAIN_CONTAINER {
            flex-direction: column;
            margin: 0;
        }
        #SIDEBAR {
            display: flex;
            flex-direction: row;
            align-items: flex-end;
            justify-content: space-between;
        }
        #SIDEBAR_TEXT {
            writing-mode: horizontal-tb;
            margin-left: 1rem;
        }
    }

    /*.name-text {
    border: solid 2px rgb(0 100 100);
  }*/
</style>
