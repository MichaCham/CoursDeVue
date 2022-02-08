<template>
    <span>{{numero}}</span>
</template>

<script>
import { defineComponent } from "vue"

export default defineComponent({
    props :{
        numero : Number
    }

})



</script>