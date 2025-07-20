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
</style>
<Navbar />
<Banner />
<div style="postion: relative; user-select: none; margin-bottom: -5px; padding: 0;">
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
    <h3>are the currency you earn for your animals in the zoo</h3>
    <br>
    <h2><span style="background-color: rgb(100,100,60)">1 MYN = 1 USD</span></h2>
</div>
<br>
