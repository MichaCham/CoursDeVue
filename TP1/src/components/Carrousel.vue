<template>

    <div>
        <img alt="Image" :src="listeImage[numer]">
        <button v-on:click="next_left"> [- suivante</button>
        <button v-on:click="next_right">suivante -></button>
    </div>
</template>

<script>
    import { defineComponent } from 'vue';
    export default defineComponent({
        data: () => {
            return {
                i: 0,
                listeImage: ["../assets/img/1.png","../assets/img/2.png","../assets/img/3.png","../assets/img/4.png","../assets/img/5.png","../assets/img/6.png"]
            }
        },
        methods:{
            next_right: function (){
                console.log(this.listeImage[this.i]);
                this.i ++;
                if(this.i >= this.listeImage.length){
                    this.i =0;
                }
            },
            next_left: function (){
                console.log(this.listeImage[this.i]);
                this.i --;
                if(this.i < 0){
                    this.i = this.listeImage.length-1;
                }
            }
        }
    }) 
</script>

<style>
img {
	width: 1000px;
}
</style>



