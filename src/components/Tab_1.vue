<template>
  <div id="tab1" class="row">
    <div class="col">
      <div class="row title dark flex-center">
        <span>HOTEL <strong>Mieres del Camín Apartamentos</strong></span>
        <img src="../assets/img/stars.png" class="img-title-right" />
      </div>
      <div class="row overflow-auto">
        <div class="radio-button-group col">
          <lxRadioButton 
              :title="item.title" 
              :description="item.description" 
              v-for="(item, index) in myJson" 
              :key="item.id" 
              :active="index === activeLiIndex"
              :index="index"
              @newactive="activeLiIndex = $event"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import lxRadioButton from './lx-radio-button.vue'
import myJson from '../assets/json/Tab_1.json'


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

