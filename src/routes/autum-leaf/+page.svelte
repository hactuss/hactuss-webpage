<script>
    //import "./../root.scss";
    import image from "$lib/assets/autum-leaf/autum leaf by hactuss.png";
</script>

<main>
    <img src={image} alt="font-screenshot" />
    <section>
        <h1>Introducing "Autum Leaf" by hactuss</h1>
        <p>
            "Autum Leaf" is a futuristic, hard to read font that is a
            combination of inspiration by the Designers Republic's wip3out font,
            and limited knowledge of Affinity. It was initially made with the
            intent of certain characters looking similar.
            This is the reason why many parts in the font feel reused for many
            characters.
        </p>
    </section>
</main>

<style>
    :global{
        :root {
            font-family: Arial, Helvetica, sans-serif;
            color: white;
        }
        body {
            background-color: black;
            text-align: center;
        }
        main{
            margin: 1em;
        }
        p,
        h1,
        h2,
        pre {
            text-align: left;
        }
        img {
            filter: invert(100%);
            text-align: center;
        }

    }
</style>
