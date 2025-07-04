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
</style>

<div id="navbar">
    <img id = "logo" src="logo.png" alt="Logo for The Zoo, a Hack Club You Ship We Ship program"/>
</div>
<div id="spacing"></div>
<div id="ysws">
    <div id="banner1">
        <br><br>
        <h2>You ship</h2>
        <h1>A SVELTE SITE</h1>
        <br><br>
    </div>
    <div id="banner2">
        <br><br>
        <h2>We ship</h2>
        <h1>A FRIDGE MAGNET</h1>
        <br><br>
    </div>
</div>
<br>
<div id="svelte">
    <h2>What is Svelte?</h2>
    <img src="favicon.svg" alt="Svelte Logo" width="100px" height="100px"/>
    <br>
    <h3>Svelte is a UI framework that uses a compiler to let you write breathtakingly concise components that do minimal work in the browser, using languages you already know — HTML, CSS and JavaScript. It’s a love letter to web development.</h3>
</div>