<template>
  <div id="app">
    <tab-nav
      :tabs="['Imutable', 'Mutable', 'Search']"
      :selected="selected"
      @selected="setSelected"
    >
      <the-tab :isSelected="selected === 'Imutable'">
        <imutable-methods></imutable-methods>
      </the-tab>
      <the-tab :isSelected="selected === 'Mutable'">
        
        <mutable-methods></mutable-methods>
      </the-tab>
      <the-tab :isSelected="selected === 'Search'">
        <search-methods></search-methods>
      </the-tab>
    </tab-nav>
  </div>
</template>

<script>
import TabNav from './components/TabNav.vue';
import TheTab from './components/TheTab.vue';

export default {
  components: { TabNav, TheTab },
  data() {
    return {
      selected: 'Imutable',
    };
  },
  methods: {
    setSelected(tab) {
      this.selected = tab;
    },
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  position: static;
}
</style>
