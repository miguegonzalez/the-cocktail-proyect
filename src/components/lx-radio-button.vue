<template>
  <div class="lx-radio-button col h-100" :class="[{'active': active}, index]" @click.stop="toogleRowActive">
    <div class="row lx-radio-button__title">{{ title }}</div>
    <div class="row lx-radio-button__description">
      <ul>
        <li v-for="(show, index) in description" :key="index">{{ show }}</li>
      </ul>
    </div>
    <div class="row lx-radio-button__button">
      <input type="radio" name="choose_scheme" value="Elegir régimen" :checked="active" /> 
      <label for="choose_scheme">Elegir régimen</label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'lx-radio-button',
  props: {
    title: String,
    description: Array,
    active: Boolean,
    index: Number,
  },
  methods: {
    toogleRowActive() {
      this.$emit('newactive', this.index)
    }
  }
}
</script>
