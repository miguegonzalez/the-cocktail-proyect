<template>
  <header>
    <div class="row">
      <a>Tab 1</a>
      <a>Tab 3</a>
    </div>
  </header>
  <body>
    <Tab1 />
    <!--<Tab3 />-->
  </body>
</template>

<script>
import Tab1 from './components/Tab_1.vue'
import Tab3 from './components/Tab_3.vue'

export default {
  name: 'App',
  components: {
    Tab1,
    Tab3,
  }
}
</script>

<style lang="scss">
  @import url('@/assets/css/main.scss');
</style>
