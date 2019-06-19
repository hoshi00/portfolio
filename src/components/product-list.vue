<template>
  <div id="container">
    <product-header
    v-bind:sortYear="sortYear"
    v-on:sortYearChanged="sortYearChanged"
    v-bind:showUseVue="showUseVue"
    v-on:showUseVueChanged="showUseVue=!showUseVue"
    ></product-header>
    <div class="card-wrapper my-gallery">
      <product
      v-for="product in filterdList"
      v-bind:product="product"
      > </product>
    </div>
  </div>
</template>

<script>
import productHeader from './product-header.vue'
import product from './product.vue'

export default {
  name: 'ProductList',
  props: ['products'],
  components: {
    'product-header': productHeader,
    'product': product
  },
  data: function () {
    return {
      sortYear: 0,
      showUseVue: false,
    }
  },
  methods: {
    sortYearChanged: function(year) {
      this.sortYear = year;
    }
  },
  computed: {
    filterdList: function() {
      let newList = [];
      for (var i = 0; i < this.products.length; i++) {
        var isShow = true;
        if (this.showUseVue && this.products[i].use !== 'Vue.js') {
          isShow = false;  // この商品は表示しない
        }

         if(this.sortYear === 1 && this.products[i].year === '2019') {
           if (isShow) {
             newList.push(this.products[i]);
           }
         }else if(this.sortYear === 2 && this.products[i].year === '2018') {
                      if (isShow) {
             newList.push(this.products[i]);
           }
         } else if (this.sortYear === 3 && this.products[i].year === '2017') {
                      if (isShow) {
             newList.push(this.products[i]);
           }
         } else if (this.sortYear === 4 && this.products[i].year === '2016') {
                      if (isShow) {
             newList.push(this.products[i]);
           }
         }else if(this.sortYear === 0) {
                      if (isShow) {
             newList.push(this.products[i]);
           }
         }
      }
      // if (this.showUseVue && this.products[i].use === 'Vue.js') {
      //   //「セール対象」チェック有りで、セール対象商品ではない場合
      //   isShow = false;  // この商品は表示しない
      // }

      return newList;
    }
  }
}
</script>

<style>

</style>
