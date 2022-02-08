<template>
  <img alt="Image" src={{listeImage[i]}}>
</template>

<script>
    import { defineComponent } from 'vue';
    export default defineComponent({
        data: () => {
            return {
                numerosImage: 0,
                listeImage: ["../img/1.png","../img/2.png","../img/3.png","../img/4.png","../img/5.png","../img/6.png"],
            }
        },
        methods:{
        }
    }) 
</script>



