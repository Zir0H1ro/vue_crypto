<template>
    <div class="sidebar">
        <nav>
            <ul>
                <li v-for="c in currencies" v-bind:key="c">
                    <a href="#">{{ c.toUpperCase() }}</a>
                </li>
            </ul>
        </nav>
        <div class="search">
            <div class="magnifier">
                <i class="fa fa-search fa-lg" aria-hidden="true"></i>
            </div>
        </div>
        <div class="twenty-four-hr d-flex">
            <div class="star">
                <i class="fas fa-star fa-lg"></i>
            </div>
            <div class="inner">
                <input type="number" disabled placeholder="24h change" />
            </div>
            <div class="inner">
                <input type="number" disabled placeholder="24h volume" />
            </div>
        </div>
        <SidebarCurrency transactionType="buy" currencyType="bitcoin" currencyAbbr="btc" :percentShift=1000.31 />
        <SidebarCurrency transactionType="sell" currencyType="bitcoin" currencyAbbr="btc" :percentShift=89.31 />
        <SidebarCurrency transactionType="buy" currencyType="monero" currencyAbbr="xmr" :percentShift=-40.31 />
        <SidebarCurrency transactionType="buy" currencyType="bitcoin" currencyAbbr="btc" :percentShift=-30.31 />
        <SidebarCurrency transactionType="buy" currencyType="bitcoin" currencyAbbr="btc" :percentShift=300.31 />
        <SidebarCurrency transactionType="buy" currencyType="monero" currencyAbbr="xmr" :percentShift=1000.31 />
        <SidebarCurrency transactionType="buy" currencyType="dash" currencyAbbr="dash" :percentShift=89.31 />
    </div>
</template>

<script>
import SidebarCurrency from './SidebarCurrency.vue'

export default {
  name: 'Sidebar',
  components:{
      SidebarCurrency
  },
  data(){
      return {
          currencies:[
              'btc',
              'eth',
              'eur',
              'usdt'
          ]
      };
  }
}
</script>