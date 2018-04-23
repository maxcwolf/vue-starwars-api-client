<template>
  <div id='app'>
      <h3 class='display-1'>{{title}}</h3>
      <h4 class='text-muted'>{{subtitle}}</h4>
      <div class="col-md-12">
        <Character
            v-for="(id, index) in initial_ids"
            :id="id" :key="index" />
      </div>

  </div>
</template>

<script>
import Character from "./components/Character.vue";
export default {
  name: "app",
  data() {
    return {
      title: "Generate Your Team",
      subtitle: "Click on a card to get a new random character",
      initial_ids: [1, 13, 14]
    };
  },
  components: {
    Character
  }
};
</script>

