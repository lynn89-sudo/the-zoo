<svelte:head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0&icon_names=pets" />
</svelte:head>
<script>
    import Navbar from "$lib/navbar.svelte";
    import Footer from "$lib/footer.svelte";
</script>
<style>
    #body {
        background-color: darkgoldenrod;

        h1 {
            padding-top: 20px;
        }
    }
</style>
<Navbar />
<div id="body">
    <h1>GUIDE</h1>
    <h2>Embark on a quest to capture your animal and master the ways of Svelte</h2>
</div>
<Footer />