<script lang="ts">
    let ufoSrc = './wd-ufo.png';

    let changeColor = function ()
    {
        if (ufoSrc == './wd-ufo.png') {
            ufoSrc = './ufo.png';
            document.body.style.backgroundImage = "url('./cosmo-backround2.jpg')";
        }
        else {
            ufoSrc = './wd-ufo.png';
            document.body.style.backgroundImage = "url('./pexels-martin-banov-4753682.jpg')";

        }
    };
</script>

<div id="ufo" on:click = {changeColor}>
    <img alt="ufo" src="{ufoSrc}">
</div>

<style>
    #ufo {
        position: fixed;
        transition: 0.3s;
        height: 100px;
        width: 100px;
        left: 18%;
        cursor: pointer;
    }

    img {
        cover: cover;
        height: inherit;
        width: inherit;
    }
</style>