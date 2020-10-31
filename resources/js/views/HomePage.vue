<template>
  <div id="app">
    <div class="homepage-container">
      <div v-for="homepage in homepage" :key="homepage.main_content">
        <Homepage :main_content="homepage.main_content" />
      </div>
    </div>
  </div>
</template>

<script>
import Homepage from '../components/Homepage.vue'

export default {
  name: 'app',
  data(){
    return {
      homepage: []
    }
  },
  components: {
    Homepage
  },
  mounted(){
    fetch('https://samuilmarinov.co.uk/wp-json/homepage/v1/page')
      .then((r) => r.json())
      .then((res) => this.homepage = res.map(x => x.acf));
  }
}
</script>

<style>
.homepage-container {
  padding-top: 60px;
  display: block;
  justify-content: space-between;
}

html, body {
    margin: 0;
    height: 100%;
    background-color: #FAFAFA;
    font-family: 'Roboto', sans-serif;
}

body {
  margin-left: 0%;
  margin-right: 0%;
}

#app > h1 {
  text-align: initial;
  color: 212121;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#footer{
  text-align: center;
  text-decoration: none;
  color: 212121;
}


</style>
