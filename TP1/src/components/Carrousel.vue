<template>


  <img alt="Image" src={{listeImage[i]}}>
  <button v-on:click="next"></button>
</template>

<script>
    import { defineComponent } from 'vue';
    export default defineComponent({
        data: () => {
            return {
                numerosImage: 0,
                listeImage: ["../img/1.png","../img/2.png","../img/3.png","../img/4.png","../img/5.png","../img/6.png"],
                monImage : listeImage[i]
            }
        },
        methods:{
            next_right: function (){
                this.numerosImage ++;
                if(this.numerosImage >= this.listeImage.length()){
                    this.numerosImage =0;
                }
            },
            next_left: function (){
                this.numerosImage --;
                if(this.numerosImage < 0){
                    this.numerosImage = this.listeImage.length();
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



