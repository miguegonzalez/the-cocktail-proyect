<template>
<div class="h-100 flex-for-column">
  <nav>
    <div class="row">
      <div class="col my-nav">
        <div class="tab" :class="{'active': !this.TabActive}" @click="changeTab()">Tab 1</div>
        <div class="tab" :class="{'active': this.TabActive}" @click="changeTab()">Tab 3</div>
      </div>
    </div>
  </nav>
  <div class="main">
    <div class="h-100">
      <Tab1 v-if="!this.TabActive" />
      <Tab3 v-else />
    </div>
  </div>
</div>
</template>

<script>
import Tab1 from './components/Tab_1.vue'
import Tab3 from './components/Tab_3.vue'

export default {
  name: 'App',
  components: {
    Tab1,
    Tab3,
  },
  data() {
    return {
      TabActive: 0,
    }
  },
  methods: {
    changeTab() {
      this.TabActive = !this.TabActive;
    }
  }
}
</script>

<style lang="scss">
  @import url('@/assets/css/main.scss');
</style>
