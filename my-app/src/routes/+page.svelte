<script>
    import Navbar from "$lib/navbar.svelte"
    let aboutLabel = $state("");
    function about(num) {
        if (num === 1) {
           aboutLabel = `<h3>
                You make a static multi-page website with Svelte, 
                and host it on Github Pages (or another deployment method).<br><br>
                Your site must be themed around an animal, real or imaginary,
                 and include both a panel with information/facts and a page with
                  an interactive version of the animal.
                <br><br>
                Additional prizes will be awarded for polished projects on
                 endangered animals or species (real).
           </h3>`;
        } else if (num === 2) {
            aboutLabel = `<h3>
                We ship you a special fridge magnet that you can put
                on your fridge or any other magnetic surface.<br><br>
                A special stickersheet will be awarded to polished projects
                 about endangered animals or species (real).
                <br><br>
                Your project will also be added to the Hack Club Zoo, an online 
                gallery of all the projects made in this program.
           </h3>`;
        }
    }
</script>
<style>
    #ysws {
        position: relative;
        text-align: center;
        width: 100%;
        height: 300px;
        user-select: none;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        overflow-x: hidden;
    }
    @media (min-width: 750px) {
        #ysws {
            height: 200px;
        }
    }

    #banner1 {
        position: absolute;
        background-color: rgb(37, 68, 37);
        width: 100%;
    }
    #banner2 {
        position: absolute;
        width: 100%;
        background-color: rgb(70, 104, 70);
        animation: slideYSWS 15s infinite ease-in-out;
    }
    @keyframes slideYSWS {
        0% {
            transform: translateX(100vw);
            opacity: 0;
        }
        28% {
            transform: translateX(100vw);
            opacity: 0;
        }
        29% {
            transform: translateX(100vw);
            opacity: 100;
        }
        30% {
            transform: translateX(100vw);
        }
        40% {
            transform: translateX(0);
        }
        75% {
            transform: translateX(0);
        }
        85% {
            transform: translateX(-100vw);
            opacity: 100;
        }
        86% {
            transform: translateX(-100vw);
            opacity: 0;
        }
        87% {
           transform: translateX(100vw);
        }
        100% {
            transform: translateX(100vw);
            opacity: 0;
        }
    }

    #about {
        background-color: rgb(6, 119, 85);
        h1 {
            font-size: 90px;
            cursor: pointer;
        }
        h1 span:first-child {
            color: rgb(150, 201, 109);
        }
        h1 span:last-child {
            color: rgb(187, 228, 187);
        }
    }
</style>

<Navbar />
<div id="ysws">
    <div id="banner1">
        <br><br><br>
        <h2>You ship</h2>
        <h1>A SVELTE SITE</h1>
        <br><br>
    </div>
    <div id="banner2">
        <br><br><br>
        <h2>We ship</h2>
        <h1>A FRIDGE MAGNET</h1>
        <br><br>
    </div>
</div>
<br><br>
<div id="svelte">
    <h2>What is Svelte?</h2>
    <img src="favicon.svg" alt="Svelte Logo" width="100px" height="100px"/>
    <br><br>
    <h3>Svelte is a web development UI framework that uses a compiler to let you write concise components that do minimal work in the browser, using language syntax you probably already know: HTML, CSS and JS (or TS).</h3>
    <h3>It's a great alternative to React, Vue, and other frameworks!</h3>
    <p>(This website was made with Svelte)</p>
    <br>
    <a href="https://svelte.dev"><button><h2>Svelte Website</h2></button></a>
    <br><br>
</div>
<br><br>
<div id="about">
    <br><br>
    <h2>What is The Zoo?</h2>
    <h3>The Zoo is a Hackclub "You Ship We Ship" (YSWS) Program</h3>
    <br>
    <p>(Click the buttons)</p>
    <h1><span><a on:click|preventDefault = {() => {about(1)}} role="button" tabindex="0">YS</a></span><span><a on:click|preventDefault = {() => {about(2)}} role="button" tabindex="0">WS</a></span></h1>
    {@html aboutLabel}
    <br><br>
</div>