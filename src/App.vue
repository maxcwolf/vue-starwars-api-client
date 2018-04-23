<template>
  <div id='app'>
      <h2>Star Wars Character and Planet Explorer</h2>
      <h4>
          <router-link class="link" to="/data/people">Pick the Characters</router-link> |
          <router-link class="link" to="/data/planets">Explore the Planets</router-link>
      </h4>
      <router-view></router-view>
  </div>
</template>


