<script>
    import asterisk from "$lib/assets/graphicdesign/asterisk.webp";
    import coral from "$lib/assets/graphicdesign/coral.png";
    import gentoo from "$lib/assets/graphicdesign/gentoo-propaganda.png";
    import hactus_poster from "$lib/assets/graphicdesign/hactus_poster.webp";
    import lost_terminal from "$lib/assets/graphicdesign/Lost Terminal Promotion Poster.webp";
    import nixos from "$lib/assets/graphicdesign/nixos-propaganda.png";
    import obnite from "$lib/assets/graphicdesign/Obnite.webp";
    import secret_code from "$lib/assets/graphicdesign/secretcodeofhactuss.png";
    import supreme_design_abuse from "$lib/assets/graphicdesign/supreme design abuse.webp";
    import phone from "$lib/assets/graphicdesign/This is a phone.webp";
    import phone_2400 from "$lib/assets/graphicdesign/This is a phone 2400.png";

    // ####################################################################################
    import "./graphicdesign.scss";
    /*
    const imageModules = import.meta.glob("$lib/assets/graphicdesign/*", {
        query: "?url",
    });
    const images = Object.entries(imageModules).map(([url]) => ({ url }));*/
    let sorted = $state(false);
    function sort() {
        sorted = !sorted;
    }
</script>

<main>
    <header>
        <h1>Hactus Design - this site is unproportional</h1>
        <button onclick={sort}>Sort</button>
    </header>
    <main>
        {#if sorted == false}
            <div class="gallery">
                <img src={asterisk} alt="" />
                <img src={coral} alt="" />
                <img src={gentoo} alt="" />
                <img src={hactus_poster} alt="" />
                <img src={lost_terminal} alt="" />
                <img src={nixos} alt="" />
                <img src={obnite} alt="" />
                <img src={secret_code} alt="" />
                <img src={supreme_design_abuse} alt="" />
                <img src={phone} alt="" />
                <img src={phone_2400} alt="" />
                <!--
                {#each images as image}
                    <img src={image.url} alt={image.url} />
                {/each}

                {#each Object.entries(imageModules2) as [_path, module]}
                    <enhanced:img src={module.default} alt="some alt text" />
                {/each}
-->
            </div>{/if}
        {#if sorted == true}
            <div class="gallery_sorted">
                <div class="sorted_category">
                    <h3>made for clients</h3>
                    <img src={lost_terminal} alt="" />
                </div>
                <div class="sorted_category">
                    <h3>self branding</h3>
                    <img src={asterisk} alt="" />
                    <img src={coral} alt="" />
                    <img src={hactus_poster} alt="" />
                    <img src={obnite} alt="" />
                    <img src={secret_code} alt="" />
                </div>
                <div class="sorted_category">
                    <h3>linux propaganda</h3>
                    <img src={nixos} alt="" />
                    <img src={gentoo} alt="" />
                </div>
                <div class="sorted_category">
                    <h3>phone related designs</h3>
                    <img src={supreme_design_abuse} alt="" />
                    <img src={phone} alt="" />
                    <img src={phone_2400} alt="" />
                </div>
            </div>
        {/if}
    </main>
</main>

<style lang="scss">
    main {
        width: 100vw;
    }
    .gallery {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .gallery_sorted {
        display: block;
    }
</style>
