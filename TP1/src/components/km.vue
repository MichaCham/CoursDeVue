<template>
  <div>
    <h3>Exemples :</h3>
    Nom : <input v-model="name" />
    Prenom : <input v-model="prenom"/>
    <span> Je suis {{ myName }} </span>
  </div>

  <div>
    <h3>TP1 exo1 : </h3>
    <p>ma distance en m: <input v-model="distance"/></p> 
    <p>mon  : <input v-model="typDistance"/></p> 
    <p>Ma disctance est {{ monKm }} {{typDistance}} </p>
  </div>
  
</template>

<script>
  import { defineComponent } from 'vue';

  export default defineComponent({
      data: () => {
          return {
              name: '',
              prenom:'',
              distance: 10,
              typDistance : 'km',

          }
      },
      computed:{
        myName(){
          return `${this.name} ${this.prenom}`;
        },

        monKm(){
          switch (this.typDistance) {
            case 'cm':
              return `${this.distance}` * 100;
            case 'km':
              return `${this.distance}` / 100;
            case 'mm':
              return `${this.distance}` * 1000;
            case 'm':
              return `${this.distance}` ;
          }
          ;
        }
      },
      methods: {
        
      }
  })


</script>
