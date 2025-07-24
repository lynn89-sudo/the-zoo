<style>
    #navbar {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        height: 105px;
        z-index: 1000;
        background-color: rgba(40, 143, 40, 0.955);
        transition: background-color 0.3s ease-in-out;
    }

    #logo {
        margin: 0 auto;
        display: block;
        width: 250px;
        height: auto;
        margin-top: 10px;
        -webkit-user-drag: none;
        -moz-user-drag: none;
        -o-user-drag: none;
        cursor: pointer;
        transition: opacity 0.3s ease-in-out; /* Transition for opacity */
    }

    @media (max-width: 750px) {
        #navbar {
            height: 70px;
        }

        #logo {
            width: 150px;
        }
    }

    @media (min-width: 750px) {
        #navbar #logo {
            position: absolute;
            left: 0;
            right: 0;
            transition: right 1s ease-in-out; /* Transition for position */
        }

        #navbar .navbutton {
            margin-top: 30px;
            background-color: darkgreen;
            border: none;
            opacity: 0;
            visibility: hidden;
            transition: opacity 1s ease-in-out;
            margin-right: 20px;
        }
    }

    #navbar .navbutton {
        opacity: 0;
        visibility: hidden;
        transition: opacity 1s ease-in-out;
        margin-right: 20px;
        color: white;
    }

    #navbar:hover {
        background-color: rgb(40, 143, 40);
    }

    #spacing {
        height: 105px;
    }

    @media (max-width: 700px) {
        #spacing {
            height: 70px;
        }
    }
</style>

<div id="navbar">
    <a href= "/the-zoo/"><img id = "logo" src="logo.png" alt="Logo"/></a>
</div>
<div id="linkto"></div>
<div id="spacing"></div>