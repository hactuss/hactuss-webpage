<script>
    import image from "$lib/assets/asterisk/front_logo.svg";
</script>

<main>
    <header class="title_card">
        <span style:background-color="red"
            >Asterisk brand is already taken.</span
        >
        <div class="title_card">
            <img
                src={image}
                alt="asterisk"
                color="white"
                width="100px"
                style:margin="5px"
            />
            <!--<p>Asterisk™ is a small graphic design studio run by hactuss.</p>-->
            <p>Asterisk™</p>
        </div>
        <!-- --
        <div class="title_card">
            <h1 class="asterisk">✱</h1>
            <div>
                <h1>Heavy asterisk</h1>
                <h3>U+2731</h3>
            </div>
        </div>
        <div class="title_card">
            <h1 class="asterisk">*</h1>
            <div>
                <h1>Asterisk</h1>
                <h3>U+002A</h3>
            </div>
        </div>
        -->
    </header>
    <div class="showcase">
        <!-- --
        <div class="showcase_pannel">
            <h2>Promotional designs</h2>
            <h6>Self introduction poster</h6>
        </div>
        -->
        <div class="showcase_pannel">
            <h2>Customer desgins</h2>
            <img
                src="https://cdn.masto.host/namtaocom/media_attachments/files/116/497/739/159/923/227/original/9b9adc120fa1cb42.png"
                alt="lt-poster"
                width="400em"
            />
            <h6>
                Promotional poster for the "Lost Terminal" podcast <br />
                <a href="https://namtao.com/@lostterminal/116497754617963752"
                    >Official post here</a
                >
            </h6>
            <!--<p class="playingcard">🂡✱</p>-->
        </div>
    </div>
    <footer>
        <div>
            <h4>hire me or sth</h4>
        </div>
    </footer>
</main>

<style lang="scss">
    :global{
        * {
            margin: 0;
            padding: 0;
            border: 0;
        }
        :root {
            font-family: Helvetica;
            font-size: 1.75rem;
        }
        /* Box Elements ====================================================================================*/
        body {
            height: 100dvh;
            /*border: solid red 1px;*/
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            /*background-color: rgb(0 0 255);*/
        }
        main {
            height: 100%;
            width: 100%;
            background-color: white;
        }
        nav,
        footer {
            background-color: black;
            color: white;
        }
        header {
            background-color: rgb(0 30 30);
            color: white;
        }

        /*Text Elements ====================================================================================*/
        a {
            mix-blend-mode: difference;
            color: white;
        }
        a::after {
            content: "⇱";
            display: inline-block;
            align-items: baseline;
            color: white;
            mix-blend-mode: difference;
        }

    }
    .showcase {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
    .showcase_pannel {
        width: 100%;
        margin: 1rem;
        text-align: center;
        background-color: rgba(0, 0, 0, 0.3);
    }
    /*.playingcard {font-size: 6em;}*/
    .title_card {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
</style>
