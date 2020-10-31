<template>
    <!-- <div class="homepage" :id="main_content">
  <p class="maincontent"><span v-html="main_content">{{ main_content }}</span></p>
  </div> -->
  <p>TEST</p>
</template>

<script>
export default {
  name: 'Homepage',
  props: {
    main_content: String
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
.homepage {
    display: flow-root;
    flex-direction: column;
    text-align: left;
    color: #212121;
}

.homepage > img {
  width: 200px;
}

@media only screen and (max-width: 800px) {
  .homepage > img {
    height: 60px;
  }
}


.homepage-img{
    border-radius: 50%;
    transition: box-shadow .3s;
    border: 4px #f6e767 solid;
}

.homepage-img:hover {
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

.homepage:hover > h3:before {
  visibility: visible;
  -webkit-transform: scaleX(1);
  transform: scaleX(1);
}
</style>
