<template>
<div id="tab3" class="h-100 flex-for-column">
  <div class="row title">Bebidas</div>
  <div class="row panel h-100">
    <div class="col flex-for-column h-100">
      <div class="row title"><div class="col">Cervezas</div></div>
      <div class="row h-100 overflow-auto">
        <div class="col">
          <lxBeerCard
              :image_url="item.image_url"
              :name_beer="item.name"
              :description="item.description"
              :food_pairing="item.food_pairing"
              :abv="item.abv"
              v-for="(item, index) in myJson"
              :key="item.id"
              :index="index"
          />
        </div>
      </div>
      <div class="pagination">
        <li v-for="page in pages" :key="page" :class="{'active': page == current_page}" @click="nextPage(page)">{{page}}</li>
      </div>
    </div> 
  </div>
</div>
  
</template>

<script>
import { computed } from '@vue/runtime-core';
import lxBeerCard from './lx-beer-card.vue';
import axios from 'axios';

const SERVER_URL = "https://api.punkapi.com/v2/beers"

export default {
  name: 'Tab_1',
  props: {},
  components: {
      lxBeerCard,
  },
  data() {
    return {
      myJson: undefined,
      nElements: undefined,
      current_page: 1,
      page: 1,
      pages: undefined,
      per_page: 10,
      isLoading: false,
    }
  },
  methods: {
    getElementsPerPage() {
      axios.get(SERVER_URL + "?page=" + this.page + "&per_page=" + this.per_page)
        .then ( datos => {
          this.myJson = datos.data;
        })
    },
    getPages() {
      axios.get(SERVER_URL)
        .then ( datos => {
          this.nElements = datos.data.length;

          if((datos.data.length % this.per_page) == 0) {
            this.pages = parseInt(datos.data.length / this.per_page);
          }
          else {
            this.pages = parseInt(datos.data.length / this.per_page) + 1;
          }
        })
    },
    nextPage(el) {
      this.page = el;
                  
      axios.get(SERVER_URL + "?page=" + this.page + "&per_page=" + this.per_page)
      .then(e => {
        if(el == this.pages) {
          let limit = parseInt(this.nElements % this.per_page);
          this.myJson = e.data.slice(limit);
        }
        else {
          this.myJson = e.data;
        }
        
        this.current_page = this.page;
      });
    },
  },
  mounted() {
    this.getElementsPerPage();
    this.getPages();
  },
}
</script>

