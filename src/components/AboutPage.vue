<template>
<div class="second_fragment">
<div class="word_about"><h2>About</h2></div>
<div class="main_text"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
    <br>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
    <br>
    <br>
    
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqu
</p></div>
</div>
</template>




<script>
</script>



<style>
@media(min-width: 800px){
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