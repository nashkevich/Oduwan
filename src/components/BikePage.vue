<template>
    <div class="fragment" ref="fragment"  >
        <div class="imgaes_details">
            <div class="image_detail" style="background-image: url(img/photo_1.jpg);"></div>
            <div class="image_detail" style="background-image: url(/img/image-13bb8b4e-3a80-4d8a-b262-facbafa4971f.jpg);"></div>
            <div class="image_detail" style="background-image: url(/img/image-682f248c-f12f-4bb9-bc00-9d9e13c9c9a5.jpg);"></div>
            <div class="image_detail" style="background-image: url(/img/image-838ee6be-18bf-4648-a3ef-13dac5ca36f0.jpg);"></div>
            <div class="image_detail" style="background-image: url(/img/image-c80683ab-9690-4cb9-bc4c-8c09bf8286d7.jpg);"></div>
        </div>
        <div class="text" :style="{position:isHere ? 'fixed' : 'absolute'}">
            <div class="name_tag">Road</div>
            <div class="main_text_bike">
                <h2 class="logo_text_bike">Tubasa <br>Grow Disk</h2>
                <p><span style="color:rgba(128, 128, 128, 1)">Geometry:</span> Custom</p>
                <p><span style="color:rgba(128, 128, 128, 1)">Routing:</span> Fully-internal / Semi-internal</p>
                <p><span style="color:rgba(128, 128, 128, 1)">Group-set:</span> Mechanical / Di2 / WiFi</p>
                <p><span style="color:rgba(128, 128, 128, 1)">Brakes:</span> Flat-mount disc</p>
                <p><span style="color:rgba(128, 128, 128, 1)">Drop outs:</span> 3D printed Ti</p>
                <p><span style="color:rgba(128, 128, 128, 1)">BB shell:</span> T47 / PF30</p>
                <p><span style="color:rgba(128, 128, 128, 1)">Max tyre size:</span> 28mm</p>
                <p><span style="color:rgba(128, 128, 128, 1)">Frame weight:</span> 820-860g (56cm)</p>
                <p><span style="color:rgba(128, 128, 128, 1)">More details:</span> Customer's sheet</p>
                <br>
                <p><span style="color:rgba(128, 128, 128, 1)">Frame-set price:</span><span class="price"> £7,450</span></p>
            </div>
        </div>
    </div>
</template>
<script>
export default{
    data(){
        return{
            isHere: false,
            movingElementTop: 50
        }
    },
    async created(){
        this.handleScroll()
    },  
    
  methods: {
    handleScroll(){
        this.$nextTick(()=>{
            window.addEventListener('scroll', this.myScrollFunction);
        })
        
    },
    myScrollFunction(){

            let frag = this.$refs.fragment
            let pos = 0
            if(frag.getBoundingClientRect()){
                pos = frag.getBoundingClientRect()
            }
            
            if(pos.y <= 0){
                this.isHere = true
            }else{
                this.isHere = false
            }
       
    }
}
}
</script>
<style scoped>
.price{
    display: inline-block;
    background-color: white;
    color: black;
    padding: 5px 15px 5px 15px;
    margin-left:5px;
}
p{
    color: white;
    opacity: 1;
    text-align: left;
    font-size: 16px;

}
.logo_text_bike{
    text-align: left;
    font-size: 64px;
    color:white;
    font-weight: 600;


}
.name_tag{
    font-size: 32px;
    color: white;
    border-top: 1px solid white;
    border-bottom: 1px solid white;
    width: 20%;
    padding: 10px;
}
.text{
    position: absolute;
    top:0;
    z-index: 10;
    width: 50%;
    margin-top: 100px;
    margin-left: 10%;
    color: white;
    font-size: 8px;
}
.image_detail{
    min-height: 350px;
    width: 100%;
    height: 100%;
    background-size: 100%;
    background-repeat: no-repeat;
}
.imgaes_details{
    display: flex;
    flex-direction: column;
    gap:10px;
    position: absolute;
    right: 5%;
    margin-top: 5%;
    width: 40%;
    height: 100%;
}
.fragment{
    position: relative;
    background-color: black !important;
    background-repeat: no-repeat;
    background-position: center;
    width: 100%;
    height: 100vh;
    opacity: 0.9;
}
</style>