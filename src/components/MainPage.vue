<template>
    <div class="logo">
        <span></span>
        <h1>ODUWAN BIKES</h1>
    </div>
    
    <div class="mobile_buttons">
        
<div class="left_buttons">
    <button @click="showButtons" class="menu-button buttons_main">Menu</button>
        <button v-if="isShowButton" class="buttons_main">Models</button>
        <button v-if="isShowButton" class="buttons_main">Order</button>
    </div>
    <div class="right_buttons">
        <button  v-if="isShowButton" class="buttons_main">Contact</button>
        <button v-if="isShowButton" class="buttons_main">Instagram</button>
    </div>
    </div>
    <div class="slogan"><h2>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</h2></div>
<div class="first_selection" >
</div>

</template>




<script>
export default{
    data(){
        return{
            isShowButton:null,
            backgrounds_images:[
                '/img/photo_1.jpg',
                '/img/photo_2.jpg',
                '/img/photo_3.jpg',
                
            ],
            indexImage:0,
            

        }
    },
    async created(){
        this.checkWindowSize()
    },  
    mounted() {
    this.changeBackground(); // Инициализация при создании компонента
    setInterval(() => this.changeBackground(), 5000); // Смена каждые 5 секунд
  },      
    methods:{
        checkWindowSize(){
            let size = window.innerWidth
            console.log(size)
            if(size > 800){
                this.isShowButton = true
            }else{
                this.isShowButton = false
            }
        },
        showButtons(){
            this.isShowButton = !this.isShowButton
            console.log(this.isShowButton)
        },
        
        async changeBackground(){
            let section = document.querySelector('.first_selection');
      section.style.backgroundImage = `url(${this.backgrounds_images[this.indexImage]})`;

      // Увеличиваем индекс, убедившись, что не выйдем за пределы массива
      this.indexImage = (this.indexImage + 1) % this.backgrounds_images.length;
            
        }
    }
}
</script>



<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@400&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@700&display=swap');
@media(min-width: 800px){
    .slogan{
        color: white;
        opacity: 1;
        z-index: 1;
        display: flex;
        justify-content: center;
        align-items: end;
        position: absolute;
        width: 100%;
        height: 90%;
        text-align: center;
    }
    .slogan h2{
        opacity: 1;
        font-weight: 400;
        font-size: 20px;
        font-family: Oswald;
        color: white;
        width: 25%;
    }
    .menu-button{
        display: none;
    }
    .logo{
    z-index: 1;
    opacity: 1;
    position: absolute;
    display: flex;
    width: 100%;
    height: 100px;
    align-items: center;
    flex-direction: column;
    
    top:4%;
   
}
.logo span{
    position: absolute;
    width: 48px;
    height: 48px;
    z-index: 1;
    background-size: 100%;
    background-image:url('/public/img/logo.png') ;
}
.logo h1{
    position: absolute;
    top:30%;
    opacity: 1;
    font-size: 42px;
    color:white;
    font-family: Oswald;
}
.buttons_main{
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
.buttons_main:hover{
    opacity: 0.8;
}
.right_buttons{
    cursor: pointer;
    z-index: 2;
    position: absolute;
    display: flex;
    justify-content: space-around;
    right: 0;
    margin-top: 1%;
    margin-right: 10%;
    width: 25%;
    
}
.left_buttons{
    cursor: pointer;
    z-index: 2;
    position: absolute;
    display: flex;
    justify-content: space-around;
    margin-top: 1%;
    margin-left: 10%;
    width: 25%;
    
    
}
}
@media(max-width: 800px){
    .slogan{
        color: white;
        opacity: 1;
        z-index: 1;
        display: flex;
        justify-content: center;
        align-items: end;
        position: absolute;
        width: 100%;
        height: 90%;
        text-align: center;
    }
    .slogan h2{
        opacity: 1;
        font-weight: 400;
        font-size: 20px;
        font-family: Oswald;
        color: white;
        width: 25%;
    }
    .menu-button{
        z-index: 10;
        top:0;
    }
    .mobile_buttons {
        position: absolute;
        margin-top: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  width:100%;
  height: 20vh; /* Это просто пример, вы можете настроить высоту по своему усмотрению */
}
    .logo{
    z-index: 1;
    opacity: 1;
    position: absolute;
    display: flex;
    width: 100%;
    height: 100px;
    align-items: center;
    flex-direction: column;
    
    top:4%;
   
}
.logo span{
    position: absolute;
    width: 48px;
    height: 48px;
    z-index: 1;
    background-size: 100%;
    background-image:url('/public/img/logo.png') ;
}
.logo h1{
    position: absolute;
    top:30%;
    opacity: 1;
    font-size: 42px;
    color:white;
    font-family: Oswald;
}
.buttons_main{
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

.left_buttons, .right_buttons {
    z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px; /* Расстояние между элементами */
}
.buttons_main:hover{
    opacity: 0.8;
}
}

body{
    background-color: black;
    padding: 0;
    margin: 0;
    overflow-x: hidden;
}
    .first_selection{
        margin: 0;
        width: 100%;
        height: 100vh;
        background-repeat: no-repeat;
        background-size:cover;
        background-position: center;
        position: relative;
        opacity: 0.7;
        transition: 1s;
        /* background-image: url("C:/Users/agz-2/Desktop/oduwan/oduwan-project/public/img/photo_3.jpg"); */
    }
</style>