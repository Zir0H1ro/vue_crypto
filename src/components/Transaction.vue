<template>
    <div class="col-12 d-flex transaction-item">
        <img v-bind:src="categoriesData.logoImg + '.png'" />
        <p>{{categoriesData.first.toUpperCase()}}/{{categoriesData.second.toUpperCase()}}</p>
        <p>{{categoriesData.date}}</p>
        <p>{{categoriesData.type}}</p>
        <p class="side" v-bind:class="categoriesData.side">{{categoriesData.side}}</p>
        <p>{{categoriesData.price}}</p>
        <p v-bind:class="categoriesData.side === 'sell' ? 'buy' : 'sell'">{{categoriesData.currPrice}}</p>
        <p>{{categoriesData.takeProfit}}</p>
        <p>{{categoriesData.amount}}</p>
        <p>{{categoriesData.total}}</p>
        <p>{{categoriesData.filled}}</p>
        <p>{{categoriesData.triggerConditions}}</p>
        <div class="cancel-btn">
            <button>Cancel</button>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        categoriesData:{
            logoImg:String,
            first:String,
            second:String,
            date:String,
            type:String,
            side:String,
            price:Number,
            currPrice:Number,
            stopLoss:Number,
            takeProfit:Number,
            amount:Number,
            total:Number,
            filled:String,
            triggerConditions:String
        }
    }
}
</script>