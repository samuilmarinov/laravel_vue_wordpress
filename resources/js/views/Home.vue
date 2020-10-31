<template>
  <div id="app">
    <div class="template-container">
      <div v-for="homepage in homepage" :key="homepage.main_content">
        <Template :read_more_link="homepage.read_more_link" :column_1_icon="homepage.column_1_icon" :column_2_icon="homepage.column_2_icon" :column_3_icon="homepage.column_3_icon" :main_content="homepage.main_content" :header_image="homepage.header_image" :header_title="homepage.header_title" :header_subtitle="homepage.header_subtitle" :main_title_after="homepage.main_title_after" :column_1_title="homepage.column_1_title" :column_1_text="homepage.column_1_text" :column_2_title="homepage.column_2_title" :column_2_text="homepage.column_2_text" :column_3_title="homepage.column_3_title" :column_3_text="homepage.column_3_text" :section_left_title="homepage.section_left_title" :section_left_text="homepage.section_left_text" :section_right_title="homepage.section_right_title" :section_right_text="homepage.section_right_text" :section_right_image_circle="homepage.section_right_image_circle"  />
      </div>
    </div>
  </div>
</template>

<script>
import Template from '../components/Template.vue'

export default {
  name: 'app',
  data(){
    return {
      homepage: []
    }
  },
  components: {
    Template
  },
  mounted(){
    fetch('https://samuilmarinov.co.uk/wp-json/homepage/v1/page')
      .then((r) => r.json())
      .then((res) => this.homepage = res.map(x => x.acf));
  }
}
</script>
