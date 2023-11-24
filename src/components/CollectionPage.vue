<template>
    
<div class="third_fragment">
    <div class="collection_images">
    <div class="bike shoss">
        <h2 class="bike_name">Shoss</h2>
        <button class="bike_button">Explore</button>
    </div>
    <div class="bike fix">
        <h2 class="bike_name">Fix</h2>
        <button class="bike_button">Explore</button>
    </div>
</div>
</div>

</template>



<script>
</script>




<style>
.bike_button{
    z-index: 1;
    cursor: pointer;
    font-family: Oswald;
    text-transform: uppercase;
    letter-spacing: 0px;
    padding:1% 6%;
    background-color: rgba(0,0,0,0.56);
    color:white;
    font-size: 20px;
    font-weight: 400;
    font-style:normal;
    border:1px solid black;
    transition: 0.5s;
}
.bike_name{
    position: relative;
    margin-top: 80%;
    color: white;
    font-size: 32px;
    font-weight: 600;
}
.shoss{
    background-image: url('/public/img/image-c80683ab-9690-4cb9-bc4c-8c09bf8286d7.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}
.fix{
    background-image: url('/public/img/photo_1.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}
.bike{
    width: 30%;
    height: 60%;
    background-color: white;
}
.collection_images{
    display: flex;
    justify-content: center;
    gap: 5%;
    align-items: center;
    position: absolute;
    margin-top: 10%;
    width: 100%;
    height: 60vh;
}
.third_fragment{
    background: url("/public/img/image-13bb8b4e-3a80-4d8a-b262-facbafa4971f.jpg");
    background-color: black !important;
    background-repeat: no-repeat;
    background-position: center;
    width: 100%;
    height: 100vh;
    background-color: white;
    opacity: 0.9;
}
</style>