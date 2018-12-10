<template>
  <div class="sidebar-item d-flex">
    <div class="currency-active col-3">
      <div class="active"></div>
    </div>
    <div class="currency-info col-3">
      <img v-bind:src="currencyType +'.png'" >
      <p>{{currencyType}}</p>
      <h3>{{ currencyAbbr.toUpperCase().trim() }}</h3>
    </div>
    <div class="currency-rates col-6">
      <h4 v-bind:class="[ Number(percentShift) >= 0 ? 'buy' : 'sell' ]"><span v-if="Number(percentShift) >= 0">+</span>{{percentShift}}%</h4>
      <p class="exchange-rate">0.00001565 / 0.13$</p>
      <p class="vol">vol.   16,577.85 BTC</p> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'SidebarCurrency',
  props: {
    transactionType: String,
    currencyType:String,
    currencyAbbr:String,
    percentShift:Number
  }
}
</script>
