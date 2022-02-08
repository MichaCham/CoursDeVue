<template>
<h3>Liste Legume</h3>
  <div>Mon forme</div>
  
  <form v-if="afficher">
    <p>nom :<input id="nom" v-model="nom" name="nom"></p>
    <p>prenom :<input id="prenom" v-model="prenom" name="prenom"></p>
    <p>naissance :<input id="naissance" v-model="naissance" name="naissance"></p>
    <p>adresse :<input id="adresse" v-model="adresse" name="adresse"></p>
    <button v-on:click="checkForm">Valider</button>
  </form>
</template>

<script>
  import { defineComponent } from 'vue';

  export default defineComponent({
    data: () => {
          return {
              nom: null,
              prenom:null,
              adresse: null,
              naissance : null,
              afficher: true
          }
      },
    methods: {
      checkForm: function (){
        if(this.nom == null || this.prenom == null || this.adresse == null || this.naissance == null){
          alert("Il manque une ou plusieur information");
        }else{
          this.afficher = false;
          alert("Félicitations, vous êtes inscrits");
        }
      }

    }
  })
</script>
