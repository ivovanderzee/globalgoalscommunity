<template>
    <div id="app">
        <div id="nav">
            <router-link to="/"><img src="./assets/logoGGC.png"></router-link>
            <div class="routers">
                <router-link to="/">Home</router-link> |
                <router-link to="/about">Over ons</router-link> |
                <router-link to="/event">Events</router-link> |
                <router-link to="/question">Vragenmuur</router-link> |
                <router-link to="/ranking">Ranking</router-link>
            </div>

            <div>
                <router-link to="/signup">Registeren</router-link>
                <router-link to="/login" class="loginBtn">Login</router-link>
                <i class="fas fa-chevron-down"></i>
            </div>
        </div>

        <div class="extraBalk"> x </div>

        <router-view @authenticated="setAuthenticated" />

        <div id="footer">
            <div id="footer-context">
                <div class="footer-colom">
                    <img src="./assets/logoGGC.png">
                </div>
                <div class="footer-colom">
                    <p class="bold">17 SDG's</p>
                    <ul>
                        <li><a href="#">Wat zijn SDG's</a></li>
                        <li><a href="/">Bekijk oplossingen</a></li>
                    </ul>
                </div>
                <div class="footer-colom">
                    <p class="bold">Community</p>
                    <ul>
                        <li><a href="/">Oplossingen</a></li>
                        <li><a href="/question">Vragenmuur</a></li>
                        <li><a href="/event">Events</a></li>
                        <li><a href="/ranking">Ranking</a></li>
                    </ul>
                </div>
                <div class="footer-colom">
                    <p class="bold">Over ons</p>
                    <ul>
                        <li><a href="#">Wat zijn SDG's</a></li>
                        <li><a href="/about">Over ons</a></li>
                        <li><a href="/adminlogin">Admin</a></li>


                    </ul>
                </div>
                <div class="footer-colom">
                    <p class="bold">Contact</p>
                    <ul>
                        <li><a href="/">Facebook</a></li>
                        <li><a href="/">Twitter</a></li>
                    </ul>
                </div>
            </div>
            <div id="footer-line"></div>
        </div>
    </div>
</template>

<script>

</script>

<style>

    *{
        margin: 0;
        padding: 0;

    }
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }

    @font-face {
        font-family: font1;
        src: url("assets/Montserrat/Montserrat-Black.ttf");
    }

    @font-face {
        font-family: font2;
        src: url("assets/Open_Sans/OpenSans-Regular.ttf");

    }

    h1{
        font-family: font1;
        font-size: 40px;

    }

    a{
        text-decoration: none;
        color: black;
    }

    p{
        font-family: font2;
        line-height: 26px;
    }

    #nav {
        padding: 5px 0;
        position: fixed;
        width: 100%;
        background-color: white;
        z-index: 9999;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        box-shadow: 0 0 10px #c6c6c6;
    }

    #nav img{
        height: 40px;
        margin-right: 5vw;
    }

    #nav a {
        font-weight: bold;
        margin: 10px;
        color: #2c3e50;
    }

    #nav a.router-link-exact-active {
        color: #388E3C;
    }

    .routers{
        width: 700px;
    }

    .loginBtn{
        /*background-color: #388E3C;*/
        border: 3px solid #388E3C;
        padding: 10px 30px;
        border-radius: 10px;
    }

    .loginBtn:hover{
        background-color: #388E3C;
    }

    /**/
    #footer{
        width: 100vw;
        padding-top: 30px;
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    #footer-context{
        width: 60vw;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    #footer-context ul{
          list-style-type: none;
    }

    #footer-context li{
       margin-top: 10px;
    }

    .footer-colom {
        flex-grow: 0.25;
        padding-bottom: 27px;
        padding-left: 77px;

    }

    @media (max-width: 770px) {
        .footer-colom {
            width: calc(74% - 29px);
            padding-bottom: 27px;
            padding-left: 0px;
        }
    }

    @media (max-width: 360px) {
        .footer-colom {
            width: calc(100% - 2px)
        }
    }

    .footer-colom img{
        height: 60px;
    }

    #footer-line{
        background-color: #388E3C;
        width: 100vw;
        padding: 4px;
    }

    .Color-green{
        color:  #388E3C;
    }

    .Color-white{
        color: white;
    }

    .bold{
        font-weight: bolder;
    }

    .extraBalk{
        width: 100vw;
        padding: 25px 0;
    }


</style>
