<template>
  <div id="app">
    <div class="badge-container">
      <div v-for="badge in markers" :key="badge.name">
        <Badge :name="badge.name" :image="badge.image" :content_main="badge.content_main" />
      </div>
    </div>
  </div>
</template>

<script>
import Badge from '../components/Badge.vue'

export default {
  name: 'app',
  data(){
    return {
      markers: []
    }
  },
  components: {
    Badge
  },
  mounted(){
    fetch('https://samuilmarinov.co.uk/wp-json/markers/v1/post')
      .then((r) => r.json())
      .then((res) => this.markers = res.map(x => x.acf));
  }
}
</script>

<style>
.badge-container {
  padding-top: 60px;
  display: block;
  padding-left:5%;
  padding-right:5%;
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

p{
  contain: content;
}
</style>
