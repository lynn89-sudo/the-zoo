<style>
    #ysws {
        position: relative;
        text-align: center;
        width: 100%;

        #banner1 {
            position: absolute;
            width: 100%;
        }
        #banner2 {
            position: absolute;
            width: 100%;
            background-color: rgb(44, 95, 44);
            animation: slideYSWS 5s ease-in-out infinite;
        }

        @keyframes slideYSWS {
            0% {
                transform: translateX(100%);
            }
            40% {
                transform: translateX(0);
            }
            80% {
                transform: translateX(-100%);
            }
            90% {
                transform: translateX(-100%);
            }
            100% {
                transform: translateX(100%);
            }
        }
    }
</style>

<div id="navbar">
    <img id = "logo" src="logo.png" alt="Logo for The Zoo, a Hack Club You Ship We Ship program"/>
</div>
<div id="spacing"></div>
<div id="ysws">
    <div id="banner1">
        <br>
        <h2>You ship</h2>
        <h1>A SVELTE SITE</h1>
    </div>
    <div id="banner2">
        <br>
        <h2>We ship</h2>
        <h1>A FRIDGE MAGNET</h1>
        <h3>(And some stickers)</h3>
    </div>
</div>