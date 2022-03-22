<template>
  <div class="row">
    <div class="col">
      <lxBeerCard 
          :image_url="show.image_url" 
          :name_beer="show.name" 
          :description="show.description" 
          :food_pairing="show.food_pairing" 
          :abv="show.abv" 
          v-for="(show, index) in myJson" 
          :key="show.id" 
          :active="index === activeLiIndex"
          :index="index"
          @newactive="activeLiIndex = $event"
      />
    </div>
  </div>
</template>

<script>
import lxBeerCard from './lx-beer-card.vue'
import myJson from './Tab_3.json'


export default {
  name: 'Tab_1',
  props: {},
  components: {
      lxBeerCard,
  },
  data() {
    return {
        activeLiIndex: null,
        myJson: myJson,
    }
  },
}
</script>

