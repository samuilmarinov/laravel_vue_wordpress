<template>
<!-- <div class="template" :id="main_content">
 <p class="maincontent">
   <span v-html="main_content">{{ main_content }}</span> 
</p>
</div> -->
<div id="page" class="hfeed site">
    <header id="masthead" class="site-header block-section biography-nav-left" role="banner"
        v-bind:style="{ 'background-image': 'url(' + header_image + ')' }">
        <div class="block-overlay-content">
            <div class="banner-section">
                <div class="container">
                    <div class="row">
                        <div class="col-md-12 col-lg-10 col-lg-offset-1">
                            <div class="author-content">
                                <div class="site-branding">
                                    <p class="site-title"><a href="https://samuilmarinov.co.uk/" rel="home">{{header_title}}</a></p>
                                    <p class="site-description">{{header_subtitle}}</p>
                                </div>
                                <div class="slider-section">
                                    <div id="banner-slider" class="carousel slide" data-ride="carousel">
                                        <!-- Wrapper for slides -->
                                        <p></p>
                                        <div class="carousel-inner" role="listbox" style="     margin-top: 0px; ">
                                            <p></p>
                                            <div class="item active" style=" ">
                                                <p></p>
                                                <div class="banner-slider-content"
                                                    style="margin-top: -60px;margin-bottom: 140px;"><br>{{main_title_after}}</div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <p>
                                    <!-- .slider-section --><br>
                                    <!--text slider end-->
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
    <section class="wrapper wrap-service">
        <div class="container">
            <div class="service-inner" style="     display: flex;     justify-content: space-between; ">
                <div class="row" style="     display: flex;     justify-content: space-between; ">
                    <div class="col-md-4">
                        <div class="service-list">
                            <div class="icon-section"> 
                            <span v-html="column_1_icon">{{ column_1_icon }}</span>
                           <!-- <i class="fa fa-desktop"></i> -->
                            </div>
                            <h3> <a href="https://samuilmarinov.co.uk/wordpress-developer/"
                                    title="WordPress developer"><br> {{ column_1_title }} </a><br> </h3>
                            <p> {{ column_1_text }} </p>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="service-list">
                            <div class="icon-section">
                             <span v-html="column_2_icon">{{ column_2_icon }}</span> 
                          <!-- <i class="fa fa-camera-retro"></i> -->
                            </div>
                            <h3> <a href="https://samuilmarinov.co.uk/photographer/" title="Photographer"><br>
                                    {{ column_2_title }}</a><br> </h3>
                            <p> {{ column_2_text }} </p>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="service-list">
                            <div class="icon-section"> 
                            <span v-html="column_3_icon">{{ column_3_icon }}</span>
                           <!-- <i class="fa fa-eye"></i> -->
                            </div>
                            <h3> <a href="https://samuilmarinov.co.uk/graphic-designer/" title="Graphic designer"><br>
                                   {{ column_3_title }} </a><br> </h3>
                               <p> {{ column_3_text }} </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
   
    <section class="wrapper wrap-about" style="display: flex; justify-content: space-between; ">
        <div class="container" style="display: flex; justify-content: space-between; ">
            <div class="col-md-6 leftcol">
                <div class="block-title">
                    <h2>{{ section_left_title }}</h2>
                    <div class="title-divider"><span></span></div>
                </div>
                <div class="about-content">
                    <p>{{ section_left_text }}</p>
                    <div class="btn-container"> 
                 <!--   <a class="button button-link" href="https://samuilmarinov.co.uk/why-hire-me/">Read More </a> -->
                    <a class="button button-link" v-bind:href="read_more_link">Read More</a>
                    </div>

                </div>
            </div>
            <div class="col-md-6 rightcol">
                <!--biography testimonial start-->
                <div class="block-title">
                    <h2> {{ section_right_title }} </h2>
                    <div class="title-divider"><span></span></div>
                </div>
                <div class="testimonial-section">
                    <div id="testimonial-slide" class="carousel slide" data-ride="carousel" data-interval="7000">
                        <!-- Indicators -->
                        <!-- Wrapper for slides -->
                        <div class="carousel-inner" role="listbox">
                            <div class="item active">
                                <div class="sayer-thumb">
                                <img :src="section_right_image_circle" alt="My spare time"> 
                                 </div>
                                <div class="testimonial-content">
                                    <p> {{ section_right_text }} </p>
                                    <div class="sayer-detail"> <span class="sayer-name"><br> My spare time </span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <p>
                    <!--biography testimonial end-->
                </p>
            </div>
        </div>
    </section>
    <p>
    </p>
    <div class="clearfix"></div>
    <p>
    <a class="biography-back-to-top" href="#page" style="display: none;"><i class="fa fa-angle-up"></i></a></p>
</div>
</template>
<script>
export default {
  name: 'Template',
  props: {
      main_content: String,
      header_image: String,
      header_title: String,
      header_subtitle: String,
      main_title_after: String,
      column_1_title: String,
      column_1_text: String,
      column_2_title: String,
      column_2_text: String,
      column_3_title: String,
      column_3_text: String,
      section_left_title: String,
      section_left_text: String, 
      section_right_title: String, 
      section_right_text: String, 
      section_right_image_circle: String,
      column_1_icon: String,
      column_2_icon: String,
      column_3_icon: String,
      read_more_link: String
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
.template {
    display: flow-root;
    flex-direction: column;
    text-align: left;
    color: #212121;
}

.template > img {
  width: 200px;
}
.wrap-service {
    padding-left: 5%;
    padding-right: 5%;
}
#testimonial-slide .item > div {
    display: flex;
}
.testimonial-content{
    display:block !important;
}
@media only screen and (max-width: 800px) {
  .template > img {
    height: 60px;
  }
  .wrap-about{
   padding-left:5%;
   padding-right:5%;
   }
}


.template-img{
    border-radius: 50%;
    transition: box-shadow .3s;
    border: 4px #f6e767 solid;
}

.template-img:hover {
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

.template:hover > h3:before {
  visibility: visible;
  -webkit-transform: scaleX(1);
  transform: scaleX(1);
}
</style>
