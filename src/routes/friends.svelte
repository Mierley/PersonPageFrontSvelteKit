<script lang="ts">
    let dogSrc = './cosmoDog.jpg';
    let dogCover = 'fill';

    async function fetchDog()
    {
        let res: Response = await fetch('https://random.dog/woof.json')
        let data: any = await res.json()
        if (data.url.includes('.mp4'))
            await fetchDog()
        else {
            dogSrc = data.url;
            dogCover = 'cover';
        }
    }
</script>

<svelte:head>
    <title>Friends</title>
</svelte:head>

<section>
    <div class="dog_container">
        <div id="dog_1" class="dog_place" on:click = {fetchDog}>
            <img src="{dogSrc}" alt="" id='dog-image-1'/>
        </div>
    </div>
</section>


<style>
    .dog_container
    {
        display: flex;
        padding: 5%;
        margin-top:5%;
        margin-right: auto;
        margin-left: auto;
        position: relative;
        width: 420px;
        height: 600px;
        text-align: center;
        opacity: 100%;
        justify-content: center;
        align-items: center;
    }
    .dog_place
    {
        padding: 0;
        box-shadow: 0 0 55px 52px #fff;
        align-items: center;
        opacity: 100%;
        height: 400px;
        width: 300px;
        background-color: #fff;;
    }

    .dog_place img
    {
        opacity: 100%;
        object-fit: fill;
        height: 100%;
        width: 100%;
        cover: "{dogCover}";
    }

    .dog_place img:hover
    {
        cursor: pointer;
        transform: scale(110%);
    }
</style>