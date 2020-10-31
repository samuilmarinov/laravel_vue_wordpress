<template>
      <div>
  <!--   <h1>Website Name</h1> -->
     <p style="text-align:center;">
            <router-link :to="{ name: 'home' }">Home</router-link>
           <router-link :to="{ name: 'blog' }">Blog</router-link> 
             <!-- <router-link :to="{ name: 'homepage' }">Wordpress Page</router-link> -->
           <router-link :to="{ name: 'users.index' }">Users</router-link> 
        </p> 
        <div class="container">
            <router-view></router-view>
        </div> 
     
       <!-- <div>
        <Footer/>
      </div> -->
    </div>
    
    
</template>
<script>
import Footer from '../components/Footer.vue'
export default {
  name: 'app',
  data(){
    return {
      footer: []
    }
  },
  components: {
    Footer
  }
}
</script>

