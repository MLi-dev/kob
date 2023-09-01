<template>
  <NavBar/>
  <router-view></router-view>
</template>

<script>
import NavBar from './components/NavBar.vue'
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap/dist/js/bootstrap" 
// import $ from "jquery"; 

export default {
  components: {
    NavBar, 
  }, 
  setup() {
    //  $.ajax({
    //   url: "http://127.0.0.1:3000/user/account/token/",
    //   type: "post",
    //   data: {
    //     username: "MYLi",
    //     password: "Test123",
    //     //confirmedPassword: "Test123",
    //   },
    //   success(resp) {
    //     console.log(resp);
    //   },
    //   error(resp) {
    //     console.log(resp);
    //   }
    // });
    //  $.ajax({
    //   url: "http://127.0.0.1:3000/user/account/info/",
    //   type: "get",
    //   headers: {
    //     Authorization: "MYLi "+"eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODk4N2I5ZGI3NDY0N…jUyfQ.k8ShaTn9CR8vW5iN3DtUi07L2O4Id_63vWggud-0XtQ"
    //   }, 
    //   success(resp) {
    //     console.log(resp);
    //   },
    //   error(resp) {
    //     console.log(resp);
    //   }
    // })

  }
}

</script>

<style>
body {
  background-image: url("@/assets/background.png");
  background-size: cover;
}
</style>
