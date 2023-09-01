<template>
  <NavBar/>
  <router-view></router-view>
</template>

<script>
import NavBar from './components/NavBar.vue'
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap/dist/js/bootstrap" 
import $ from "jquery"; 

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
     $.ajax({
      url: "http://127.0.0.1:3000/user/account/info/",
      type: "get",
      headers: {
        Authorization: "Bearer "+"eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Yzc2YzlkNGE2M2I0ZTRlYjIzNzI3M2QxMTc5N2E5ZCIsInN1YiI6IjciLCJpc3MiOiJzZyIsImlhdCI6MTY5MzU4NzUyOCwiZXhwIjoxNjk0Nzk3MTI4fQ.YTV2yS-ZmkXayYf9J20DkHCEBKTIf4JcEIUY4Ff4TdQ"
      }, 
      success(resp) {
        console.log(resp);
      },
      error(resp) {
        console.log(resp);
      }
    })

  }
}

</script>

<style>
body {
  background-image: url("@/assets/background.png");
  background-size: cover;
}
</style>
