<template>
    <div class="main-content">
        <div class="content-top-bar d-flex col-12">
            <div class="d-flex col-9">
                <img v-bind:src="currencySrc.name + '.png'"/>
                <h4>{{currencySrc.abbr}}/{{currencyTarget}}</h4>
                <h5 v-bind:class="recommendedAction">{{exchangeRate}}<span v-if="recommendedAction==='buy'"><i class="fa fa-caret-up fa-lg"></i></span><span v-if="recommendedAction==='sell'"><i class="fa fa-caret-down fa-lg"></i></span></h5>
                <div class="fa-wrapper">
                    <i class="fa fa-info-circle fa-lg"></i>
                </div>
                <div class="twenty-four-dropdowns d-flex">
                    <div v-for="param in twentyFourParams" v-bind:key="param">
                        <p>{{param.name}}</p>
                        <h6 v-bind:class="param.classes">{{param.value}}</h6>
                    </div>
                </div>
            </div>
            <div class="d-flex market-nav col-3">
                <div class="col-4 market-nav-item" v-for="t in tradeOptions" v-bind:key="t">
                    {{t.toUpperCase()}}
                </div>
            </div>
        </div>
        <div class="d-flex graph-and-market">
            <div class="graph-data col-9">
                <img v-bind:src="graphContent" />
            </div>
            <div class="market col-3">
                <PriceRegulator operationType="buy" :price=16150.00 />
                <PriceRegulator operationType="sell" :price=9545.00 />
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
import PriceRegulator from './PriceRegulator.vue'
import Footer from './Footer.vue'

export default {
    name: 'MainContent',
    components:{
        PriceRegulator,
        Footer
    },
    data(){
        return {
            currencySrc:{
                name:'bitcoin',
                abbr:'btc'
            },
            currencyTarget:'usd',
            exchangeRate:'9,890.30',
            recommendedAction:'buy',
            twentyFourParams:[
                {
                    name:'24h change',
                    value:-13.42,
                    classes:{
                        'buy':true
                    }
                },
                {
                    name:'24h volume',
                    value:0.003991,
                    classes:{

                    }
                },
                {
                    name:'24h high',
                    value:0.003991,
                    classes:{

                    }
                },
                {
                    name:'24h low',
                    value:0.003991,
                    classes:{

                    }
                }
            ],
            graphContent:'exchange_graph_img.jpg',
            tradeOptions:[
                'market',
                'limit',
                'stop-limit'
            ]
        }
    }
}
</script>