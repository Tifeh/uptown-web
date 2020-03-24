<script>
    let visible = false;
    import LeftComponent from './ScreenPage.svelte'
    import RightComponent from './Download.svelte'
    import Footer from './Footer.svelte'
</script>


<main>
    <section class="bodyContainer">
        <LeftComponent />
        <RightComponent/>
    </section>
    <Footer />
</main>



<style>
    :global(body) {
        background-color: #FFFFFF;
    }
    main {
        display: flex;
        height: 100%;
        flex-direction: column;
    }

    .bodyContainer {
        display: flex;
        flex: 1;
        justify-content: center;
        align-items: center;
    }

    @media (min-width: 640px) {
        main {

            max-width: none;
        }
    }
</style>
