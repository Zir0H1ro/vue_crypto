<template>
    <div class="footer">
        <nav>
            <ul>
                <li v-for="cat in categories" v-bind:key="cat">
                    <a href="#">{{cat.toUpperCase()}}</a>
                </li>
            </ul>
        </nav>
        <Transaction v-for="item in items" v-bind:key="item" :categoriesData="item" />
    </div>
</template>

<script>
import Transaction from './Transaction.vue'

export default {
    name: 'Footer',
    components:{
        Transaction
    },
    data(){
        return {
            categories:[
                'Open orders',
                'Order history',
                'Trade history'
            ],
            items:[
                {
                    'logoImg':'monero',
                    first:'xpr',
                    second:'btc',
                    'date':'12-29 15:56:00',
                    'type':'limit',
                    'side':'sell',
                    'price':0.00145657,
                    'currPrice':0.00145657,
                    'stopLoss':0.00145657,
                    'takeProfit':0.00145657,
                    'amount':4,
                    'total':5,
                    'filled':'String',
                    'triggerConditions':'GTC'
                },
                {
                    'logoImg':'dash',
                    'first':'Dash',
                    'second':'btc',
                    'date':'12-29 15:56:00',
                    'type':'limit',
                    'side':'buy',
                    'price':0.00145657,
                    'currPrice':0.00145657,
                    'stopLoss':0.00145657,
                    'takeProfit':123,
                    'amount':4,
                    'total':5,
                    'filled':'String',
                    'triggerConditions':'GTC'
                },
                {
                    'logoImg':'dash',
                    'first':'Dash',
                    'second':'Btc',
                    'date':'12-29 15:56:00',
                    'type':'limit',
                    'side':'sell',
                    'price':0.00145657,
                    'currPrice':0.00145657,
                    'stopLoss':123,
                    'takeProfit':0.00145657,
                    'amount':4,
                    'total':5,
                    'filled':'String',
                    'triggerConditions':'GTC'
                }
            ]
        };
    }
}
</script>