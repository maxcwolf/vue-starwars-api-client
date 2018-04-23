<template>
  <div id='app'>
      <h3 class='display-1'>{{title}}</h3>
      <h4 class='text-muted'>{{subtitle}}</h4>
      <h4>
          <router-link class="link" to="/data/people">Pick the Characters</router-link> |
          <router-link class="link" to="/data/planets">Explore the Planers</router-link>
      </h4>
      <router-view></router-view>
      <div class="col-md-12">
        <Character
            v-for="(id, index) in initial_ids"
            :id="id" :key="index" />
      </div>

  </div>
</template>

<script>
import Item from "./components/Item";
export default {
  name: "app",
  components: {
    Item
  },
};
</script>

