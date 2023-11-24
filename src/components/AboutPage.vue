<template>
<div class="second_fragment">
<div class="word_about"><h2>Community</h2></div>
<div class="main_text"><p>Oduwan is not bikes. 
Oduwan is a friend club 
and community bound by 
passion to push the fuck 
out of bikes and have fun

    <br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
    <br>
    <br>
    
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqu
</p>
<div class="img_about"  style="background-image: url(/img/image-c80683ab-9690-4cb9-bc4c-8c09bf8286d7.jpg);"></div></div>
</div>
</template>




<script>
</script>



<style>
@media(min-width: 800px){
    .img_about{
        width: 60%;
        height: 100%;
    }
    .main_text{
        z-index: 1;
        position: absolute;
        margin: 0;
        width: 100%;
        height: 90%;
        display:flex;
        justify-content:flex-start;
        margin-top: 4%;
        margin-left: 20%;
        align-items: center;
    }
    .main_text p {
        overflow: hidden;
        height: 60%;
        text-align: left;
        font-size: 36px;
        font-family: Oswald;
       word-break: break-all;
        width: 50%;
    }
    .word_about{
        position: absolute;
        width: 50%;
        height: 40%;
        margin-top: 5%;
        
    }
   .word_about h2{
    margin: 0;
        color: black;
        text-transform: uppercase;
        font-size: 100px;
        font-weight: 700;
        
    }
}

.second_fragment{
    width: 100%;
    height: 100vh;
    background-color: white;
    opacity: 0.9;
}
</style>