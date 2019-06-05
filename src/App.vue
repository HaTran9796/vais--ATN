<template>
  <div id="app">
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
      
      <div class="home" v-if="isAccecToken">
        <router-view/>
      </div>
      <div class="login" v-else>
        <!-- Chưa có access token
        Hiện trang login -->
        <Login :path="path"></Login> <!-- :path: là dữ liệu bên trang con -->
      </div>

    </div>
    
  </div>
</template>
<script>
import Login from '@/views/Login.vue'
export default {
  data() {
    return {
      isAccecToken: false,
      access_token: window.localStorage.getItem("access_token"),
      path: "http://konda-api-dev.vais.vn",
    }
  },
  components: {
    Login
  },
  mounted(){
    if(this.access_token != "" && typeof this.access_token != "undefined" ){
      if(this.access_token == null){
        window.localStorage.setItem("access_token", "");
        window.location.replace('/');
      }
      console.log(this.access_token)
      this.isAccecToken = true;
    }
    else 
    {
      this.isAccecToken = false // have not a access_token => login
      this.$router.push('/');
      this.isAccecToken = false;
    }
  }
}
</script>