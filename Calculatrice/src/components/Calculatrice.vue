<template>
<h1>Calculatrice</h1>
    <EcranCalculatrice/>
    <BoutonCalculatrice :numero="valeurBouton"/>
</template>

<script>
import { defineComponent } from "vue"
import EcranCalculatrice from "./EcranCalculatrice.vue"
import BoutonCalculatrice from "./BoutonCalculatrice.vue"

export default defineComponent({
    valeurBouton: 9,
    components: { EcranCalculatrice, BoutonCalculatrice }
})



</script>