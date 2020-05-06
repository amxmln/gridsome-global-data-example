<template>
  <Layout :darkMode="$root.pageDark">
    
      <!-- Learn how to use images here: https://gridsome.org/docs/images -->
      <g-image alt="Example image" src="~/favicon.png" width="135" />

      <h1>Hello, world! (Nav should be light)</h1>

      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores</p>

      <p class="home-links">
        <a href="https://gridsome.org/docs/" target="_blank" rel="noopener">Gridsome Docs</a>
        <a href="https://github.com/gridsome/gridsome" target="_blank" rel="noopener">GitHub</a>
      </p>
    
  </Layout>
</template>

<script>
export default {
  created() {
    this.$root.pageDark = this.$page.data.dark;
  },
  metaInfo: {
    title: "Hello, world!"
  }
};
</script>

<page-query>
query {
  data: pageContent(id: "home") {
    dark
  }
}
</page-query>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
