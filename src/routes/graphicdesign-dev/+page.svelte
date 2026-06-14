<script>
    import "./graphicdesign.scss";
    import introduction from "$lib/assets/graphicdesign/hactus_poster.webp";
    import asterisk from "$lib/assets/graphicdesign/asterisk.webp";
    import obnite from "$lib/assets/graphicdesign/Obnite.webp";
    import coral from "$lib/assets/graphicdesign/coral.png";
    import secret_code from "$lib/assets/graphicdesign/secretcodeofhactuss.png";
    import gentoo_propaganda from "$lib/assets/graphicdesign/gentoo-propaganda.png";
    import nixos_propaganda from "$lib/assets/graphicdesign/nixos-propaganda.png";
    /*
    const imageModules = import.meta.glob("$lib/assets/graphicdesign/*");
    let ar = $state([]);
    for (const modulePath in imageModules) {
        imageModules[modulePath]().then(() => {
            ar = [modulePath];
            console.log(ar);
        });
        }*/
</script>

<!-- --
<main>
    <header>
        <h1>Hactus Design</h1>
    </header>
    <main>
        <div class="gallery">
            {#each ar as source}
                <img src={source} alt="" />
            {/each}
        </div>
    </main>
</main>
-->
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
