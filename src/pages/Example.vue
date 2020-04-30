<template>
  <div class="layout">
    <h1>Example (Nav should be dark)</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </div>
</template>

<script>
export default {
  created() {
    this.$root.pageDark = this.$page.data.dark;
  },
  metaInfo: {
    title: 'Example'
  }
}
</script>

<page-query>
query {
  data: pageContent(id: "example") {
    dark
  }
}
</page-query>
