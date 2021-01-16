<template>
  <div class="home">
    <Header></Header>      
     <p>{{item}}</p>
     <div id="app">
       <p>Address:</p>
     </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import axios from "axios";
export default {
  data() {
    return {
      
      text: ""
    };
  },
  methods:{
      async item() {
      const item = await axios.get(`https://apis.postcode-jp.com/api/v4/postcodes/郵便番号apiKey=V0DXRtKvacz59kMqfc2RTVZIeUuNpLB0PhtqsaX`);
      console.log(item);
     }
  },
  components: {
    Header
  }
}
</script>
