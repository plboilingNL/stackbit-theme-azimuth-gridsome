<template>
  <Layout>
    <BasicPage :data="data" />
  </Layout>
</template>

<script>
import BasicPage from "../components/BasicPage"
export default {
  metaInfo: {
    title: 'Style Guide - Stackbit Azimuth Theme'
  },
  computed: {
    data() {
      return this.$static.aboutData.edges[0].node;
    },
  },
  components: {
    BasicPage
  }
}
</script>

<static-query>
  query aboutData {
    aboutData: allaboutData {
      edges {
        node {
        	title
        	subtitle
        	content
          img_path
        }
      }
    }
  }
</static-query>