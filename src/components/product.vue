<template>
  <figure class="card">
    <a target="_blank" href="https://www.google.co.jp/search?ei=7ZnXXOTYH4STr7wPp_Kz8AU&q=TIREHOOD&oq=TIREHOOD&gs_l=psy-ab.3..35i39l2j0l6.26126.26126..26920...0.0..0.149.149.0j1......0....2j1..gws-wiz.ZXG1_twO5Gk"
      data-size="980x668" class="card-image">
      <img v-bind:src="product.image" alt="">
    </a>
    <figcaption class="card-caption">
      <div class="card-title-wrap">
        <p class="card-caption-title">{{product.name}}</p>
        <p class="card-caption-year">{{product.year}}</p>
      </div>
      <p class="card-caption-category">category:
        <span>{{product.category}}</span>
      </p>
      <p class="card-caption-use">use:
        <span>{{product.use}}</span>
      </p>
      <p class="card-caption-info">info:
        <span>{{product.info}}</span>
      </p>
    </figcaption>
  </figure>
</template>

<script>
export default {
  name: 'product',
  props: ['product']
}
</script>

<style>

</style>
