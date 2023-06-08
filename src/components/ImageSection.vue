<template>
    <div class="logos">
        <div v-for="(image,index) in imageData" :key="index"  class="logo hidden">
            <img :class="{active:index}" :src=image alt="" srcset="" />
        </div>
        
    </div>
</template>


<script>
export default{
    data() {
        return {
            imageData:{
                image1:require("../assets/images/1.jpg"),
                image2:require("../assets/images/2.jpg"),
                image3:require("../assets/images/3.jpg"),
                image4:require("../assets/images/4.jpg"),
            }
        }
    },
}
</script>
