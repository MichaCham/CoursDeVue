<template>
<div>
  <h1>Clone Tweeter</h1>
  <div  v-for="tweet in tweets">
    <h1>{{}}</h1>
      <p>{{tweet.message}}</p>
      <p>{{this.msg_error}}</p>
  </div>
</div>


</template>

<script>
import axios from "axios";
import { defineComponent, resolveDynamicComponent } from 'vue';

export default defineComponent({
  data: () => {
    return {
      tweets: [],
      msg_error: "",
      users : []
    }
  },
  mounted() {
  axios.get("https://fges-twitter-clone.herokuapp.com/allTweets", {
    headers: {
      "x-fges-user-key": "NlhhqTHGrxVT2l8oOU2lx5oEN4kVJPuK",
    },
  })
  .then((result) => {
    console.log(result.data);
    this.tweets = result.data;
  })
  .catch((error) => {
    this.tweets = error
  });
  axios.get("https://fges-twitter-clone.herokuapp.com/users",{
    headers:{
      "x-fges-user-key": "NlhhqTHGrxVT2l8oOU2lx5oEN4kVJPuK",
    },
  })
  .then((result)=>{
    this.users = result.data;
  })
  .catch((error) => {
    this.users = error
  });
}

});




</script>
