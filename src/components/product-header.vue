<template>
  <header>
    <div class="sort-wrap">
        <div class="sort">
          <label for="sort">年： </label>
          <select id="sort" class="sorting" v-bind:value="sortYear" v-on:change="$emit('sortYearChanged', parseInt($event.target.value))">
            <option value="0" selected>2019～2016</option>
            <option value="1">2019</option>
            <option value="2">2018</option>
            <option value="3">2017</option>
            <option value="4">2016</option>
          </select>
        </div>
      <div class="condition">
        <div class="skill">
           使用：
          <label>
            <input type="checkbox" v-bind:checked="showUseVue" v-on:change="$emit('showUseVueChanged')"> Vue.js</label>
          </div>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
    name: 'ProductHeader',
    props: ['sortYear', 'showUseVue']
  }
</script>

<style>


</style>
