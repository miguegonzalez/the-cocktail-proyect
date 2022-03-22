<template>
  <div class="row">
    <lxRadioButton 
        :title="show.title" 
        :description="show.description" 
        v-for="(show, index) in myJson" 
        :key="show.id" 
        :active="index === activeLiIndex"
        :index="index"
        @newactive="activeLiIndex = $event"
    />
  </div>
</template>

<script>
import lxRadioButton from './lx-radio-button.vue'
import myJson from './Tab_1.json'


export default {
  name: 'Tab_1',
  props: {},
  components: {
      lxRadioButton,
  },
  data() {
    return {
        activeLiIndex: null,
        myJson: myJson,
    }
  },
}
</script>

