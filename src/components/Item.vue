<template>
  <div class='col-md-4' @click="switchItem">
      <div class="item-card">
          <div class="card-block">
              <h4 class="card-title">{{item.name}}</h4>
              <div v-for="(value, key, index) in item" :key="index">
                <div v-if="index < 5" class="">
                  <strong> {{key}}</strong>: {{value}}
                </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  props: ["item"],
  data() {
    return {
      character: {}
    };
  },
  methods: {
    switchItem() {
      let random_id = Math.floor(Math.random() * 83) + 1;
      this.fetchCharacter(random_id);
    }
  },
  created() {
    this.fetchCharacter(this.id);
  }
};
</script>
