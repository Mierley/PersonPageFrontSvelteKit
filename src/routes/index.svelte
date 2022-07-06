<script context="module" lang="ts">
    export const prerender = true;
</script>

<script lang="ts">

</script>

<svelte:head>
    <title>About me</title>
</svelte:head>

<section>
    <div id = "link_container">
        <p id = "title_block">Social media</p>
        <div class="photo"> <img src="./I_green-removebg-preview.png"></div>
        <div class="box"><a href = https://github.com/Mierley><div class = "white_star git" id="start"><img class = "icon" src="./git.png"></div></a></div>
        <div class="box"><a href = https://github.com/Mierley><div class = "white_star instagram" id ="end"><img class = "icon" src="./instagram.png"></div></a></div>
        <div class="box"><a href = https://github.com/Mierley><div class = "white_star telegram"><img class = "icon" src="./telegram.png"></div></a></div>
        <div class="box"><a href = https://github.com/Mierley><div class = "white_star vkontakte"><img class = "icon" src="./free-icon-vk-725349.png"></div></a></div>
    </div>
</section>

<style>
    section
    {
        display: flex;
    }

    .box
    {
        background-color: #333333;
        border: #333333;
    }

    #link_container
    {
        background: black;
        box-shadow: 0 0 30px 30px black;
        padding-right: 5%;
        margin-top:5%;
        margin-right: auto;
        margin-left: auto;
        position: relative;
        width: 420px;
        height: 600px;
        text-align: center;
    }
    .white_star
    {
        z-index: 8;
        box-shadow: 0 0 55px 52px #fff;
        position: absolute;
        display: flex;
        justify-content: center;
        height: 55px;
        width: 55px;
        background-color: aliceblue;
        clip-path: polygon(50% 0%, 68% 26%, 98% 35%, 80% 61%, 79% 91%, 51% 83%, 21% 91%, 21% 61%, 2% 35%, 33% 27%);
        transition: transform .7s ease-in-out;
    }
    .white_star:hover
    {
        background-color: yellow;
        transform: rotate(360deg) scale(2);
    }
    #title_block
    {
        position: absolute;
        color: aquamarine;
        align-items: center;
    }
    .icon
    {
        width: 25px;
        height: 25px;
        margin:auto;
        display: block;
    }
    .git
    {
        top: 60px;
        left: 45px;
    }
    .vkontakte
    {
        top: 220px;
        left: 95px;
    }
    .instagram
    {
        top: 420px;
        left: 15px;
    }
    .telegram
    {
        top: 320px;
        left: 375px;
    }
</style>
