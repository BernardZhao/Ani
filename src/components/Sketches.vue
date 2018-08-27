<template>
  <div class="sketches">
    <h1 is="sui-header">Sketches</h1>
    <sui-card-group :items-per-row="3">
      <sui-card v-for="sketch in sampleSketches" :key="sketch.uuid">
        <sui-image src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ea/Van_Gogh_-_Starry_Night_-_Google_Art_Project.jpg/1280px-Van_Gogh_-_Starry_Night_-_Google_Art_Project.jpg" />
        <sui-card-content>
          <sui-card-header>Sketch Title</sui-card-header>
          <sui-card-meta>Author</sui-card-meta>
          <sui-card-description>
            Description
          </sui-card-description>
        </sui-card-content>
        <sui-card-content extra>
          <sui-icon name="user" /> # of Contributors
          <span slot="right">Date created</span>
          </sui-card-content>
      </sui-card>
    </sui-card-group>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleSketches: [
        {uuid: "1"},
        {uuid: "2"},
        {uuid: "3"},
        {uuid: "4"},
        {uuid: "5"},
        {uuid: "6"},
        {uuid: "7"},
        {uuid: "8"},
        {uuid: "9"},
        {uuid: "10"},
      ]
    }
  }
}
</script>

<style scoped>
.sketches {
  padding: 5%;
}
</style>