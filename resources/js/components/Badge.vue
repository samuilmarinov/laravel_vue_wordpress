<template>
  <div class="badge" :id="name">
    <img class="badge-img" :src="image" />
    <h3>{{ name }}</h3>
    <p class="maincontent"><span v-html="content_main">{{ content_main }}</span></p>
  </div>
</template>

<script>
export default {
  name: 'Badge',
  props: {
    name: String,
    image: String,
    content_main: String 
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.maincontent{
  text-align: initial;
}
.maincontent > img{
  width:500px;
}
.badge {
    display: flow-root;
    flex-direction: column;
    text-align: left;
    color: #212121;
}

.badge > img {
  width: 200px;
}

@media only screen and (max-width: 800px) {
  .badge > img {
    height: 100px;
width:100px;
  }
}


.badge-img{
    border-radius: 50%;
    transition: box-shadow .3s;
    border: 4px #f6e767 solid;
}

.badge-img:hover {
  box-shadow: 0 0 11px rgba(33,33,33,.6); 
}

h3 {
  position: relative;
  text-decoration: none;
 
}

h3:before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  bottom: -5px;
  left: 0;
  background-color: #000;
  visibility: hidden;
  -webkit-transform: scaleX(0);
  transform: scaleX(0);
  -webkit-transition: all 0.3s ease-in-out 0s;
  transition: all 0.3s ease-in-out 0s;
}

.badge:hover > h3:before {
  visibility: visible;
  -webkit-transform: scaleX(1);
  transform: scaleX(1);
}
</style>
