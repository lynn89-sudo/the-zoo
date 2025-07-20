<svelte:head>
    {#each [1,2,3,4,5] as n}
        <link rel="preload" href={`boba/bobaD${n}.png`} as="image" />
    {/each}
    {#each [1,2,3,4,5] as n}
        <link rel="preload" href={`boba/bobaV${n}.png`} as="image" />
    {/each}
</svelte:head>
<script>
    import Navbar from "$lib/navbar.svelte"
    import Banner from "$lib/banner.svelte"
    import { onMount } from "svelte";

    let width = $state(true);
    let select1 = $state("bobaD");
    onMount(function() {
        if (window.matchMedia("(max-width: 750px)").matches) {
            width = true;
        }
        else {
            width = false;
        }


        function resize(e) {
            if (window.matchMedia("(max-width: 750px)").matches) {
                width = true;
            }
            else {
                width = false;
            }

            if (!width) {
                select1 = "bobaD"; //D
            }
            else {
                select1 = "bobaV";
            }
        }
        resize(window.matchMedia("(max-width: 750px)").matches);
    })
</script>
<style>
    #b1 {
        animation: bee1 3s ease-in-out infinite;
    }
    #b2 {
        animation: bee2 3.5s ease-in-out infinite;
    }
    @keyframes bee1 {
        0% {
            transform: translateY(0)
        }
        50% {
            transform: translateY(30px)
        }
        100% {
            transform: translateY(0)
        }
    }
    @keyframes bee2 {
        0% {
            transform: translateY(0)
        }
        50% {
            transform: translateY(-15px)
        }
        100% {
            transform: translateY(0)
        }
    }

    button {
        border: none;
        background-color: rgb(80, 69, 9);
    }
    button:hover {
        color: white;
        background-color: rgb(128, 111, 16);
    }

    #svelte {
        padding-top: 50px;
        padding-bottom: 30px;
        padding-left: 20px;
        padding-right: 20px;
        background-color: rgb(14, 32, 14);

        img {
            width: 100px;
            height: 100px;
            cursor: pointer;
            transition: transform 0.5s ease-in-out;
        }
    }
    #svelte img:hover {
        transform: rotate(7.5deg);

    }
    #svelte button {
        background-color: rgb(44, 68, 44);
    }
    #svelte button:hover {
        background-color: rgb(38, 114, 38);
    }

    #countdown {
        padding-top: 50px;
        padding-bottom: 30px;
        padding-left: 20px;
        padding-right: 20px;
        background-color: rgb(7, 83, 77);

        img {
            width: 50%;
            height: auto;
            margin: 0 auto;
            display: block;
            transition: width 0.7s ease-in-out;
        }
        img:hover {
            cursor: grab;
            width: 53.5%;
        }
    }
    @media (max-width: 750px) {
        #countdown img {
            width: 80%;
        }
        #countdown img:hover {
            width: 90%;
        }
    }
</style>
<Navbar />
<Banner />
<div style="postion: relative; user-select: none; margin-bottom: -5px; padding: 0; overflow: clip;">
    <img src="boba/{ select1 }1.png" style="position: absolute; left: 0; right: 0; width: 100%; height: auto;" alt="Overlay 1"/>
    <img src="boba/{ select1 }2.png" style="position: absolute; left: 0; right: 0; width: 100%; height: auto;" alt="Overlay 2"/>
    <img id="b1" src="boba/{ select1 }3.png" style="position: absolute; left: 0; right: 0; width: 100%; height: auto;" alt="Overlay 3"/>
    <img id="b2" src="boba/{ select1 }4.png" style="position: absolute; left: 0; right: 0; width: 100%; height: auto;" alt="Overlay 4"/>
    <img src="boba/{ select1 }5.png" style="position: absolute; left: 0; right: 0; width: 100%; height: auto; -webkit-user-drag: none; -moz-user-drag: none" alt="Overlay 5"/>
</div>
<div>
    <img src="boba/{ select1 }1.png" style="display: hidden; width: 100%; height: auto;" alt="Blank"/>
</div>
<div style="background-color: rgb(230, 177, 30); color: white; padding: 20px;">
    <br>
    <h2 style="font-size: 70px;">Mynts</h2>
    <h3>are the currency you earn for your animals in the zoo. The better your submissions are, the more mynts you earn</h3>
    <br>
    <h2><span style="background-color: rgb(100,100,60)">1 MYN = 1 USD</span></h2>
    <br><br>
    <button onclick={ window.location.href = "mynts"}><h2>How do I earn mynts?</h2></button>
</div>
<div id="svelte">
    <h2>What is Svelte?</h2>
    <a href="https://svelte.dev"><img src="favicon.svg" alt="Svelte Logo"/></a>
    <br><br>
    <h3>Svelte is a web development UI framework that uses a compiler to let you write concise components that do minimal work in the browser, using language syntax you probably already know: HTML, CSS and JS (or TS).</h3>
    <h3>It's a great alternative to React, Vue, and other JS frameworks!</h3>
    <p>(This website was made with Svelte)</p>
    <br>
    <a href="https://svelte.dev"><button><h2>Visit the Svelte Website</h2></button></a>
    <br><br>
</div>
<div id="countdown">
    <h2>When can I start?</h2>
    <br>
    <h3>This YSWS is not active or official yet. Check back here for updates soon!</h3>
    <h4>(Last updated, July 25th)</h4>
    <br>
    <img src="whale.png" alt="Whale Plushie"/>
</div>

