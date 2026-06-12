<script>
    import "./graphicdesign.scss";
    import introduction from "$lib/assets/graphicdesign/hactus_poster.webp";
    import asterisk from "$lib/assets/graphicdesign/asterisk.webp";
    import obnite from "$lib/assets/graphicdesign/Obnite.webp";
    import coral from "$lib/assets/graphicdesign/coral.png";
    import secret_code from "$lib/assets/graphicdesign/secretcodeofhactuss.png";
    import gentoo_propaganda from "$lib/assets/graphicdesign/gentoo-propaganda.png";
    import nixos_propaganda from "$lib/assets/graphicdesign/nixos-propaganda.png";
</script>

<main>
    <header>
        <h1>Hactus Design</h1>
    </header>
    <main>
        <div class="gallery">
            <img src={introduction} alt="introduction" />
            <img src={asterisk} alt="asterisk" />
            <img src={obnite} alt="obnite" />
            <img src={coral} alt="coral" />
            <img src={secret_code} alt="secret_code" />
            <img src={gentoo_propaganda} alt="gentoo_propaganda" />
            <img src={nixos_propaganda} alt="nixos_propaganda" />
            <img
                src="https://cdn.masto.host/namtaocom/media_attachments/files/116/497/739/159/923/227/original/9b9adc120fa1cb42.png"
                alt="lost_terminal"
            />
        </div>
    </main>
</main>

<style>
    main {
        width: 100vw;
    }
    .gallery {
        display: flex;
        flex-wrap: wrap;
        /*flex-direction: column;
        width: 100%;

        justify-content: center;
        align-items: center;*/
    }
</style>
