<template>
  <h1>HI Yassir</h1>
</template>

<script>
import axios from "axios";
import { onMounted } from "vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  setup() {
    const GetData = () => {
      // alert("rrr");
      axios
        .get("https://69f4-105-157-184-192.ngrok-free.app/user")
        .then((response) => {
          console.log(response); // Log the entire response object
        })
        .catch((error) => {
          console.error(error); // Log any errors
        });
    };
    onMounted(() => {
      GetData();
    });

    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
