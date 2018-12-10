<template>
    <div class="price-regulator d-flex">
        <div class="minus">
            <i class="fas fa-minus-circle" v-bind:class="operationType"></i>
        </div>
        <div class="main" v-bind:class="operationType">
            <div v-if="operationType === 'buy'">
                <i v-bind:class="operationType" class="fa fa-caret-up fa-lg"></i>
            </div>
            <h6 v-bind:class="operationType">{{operationType}}</h6>
            <p v-bind:class="operationType">Price</p>
            <h5 v-bind:class="operationType">{{price.toString()}}</h5>
            <div v-if="operationType === 'sell'">
                <i v-bind:class="operationType" class="fa fa-caret-down fa-lg"></i>
            </div>
        </div>
        <div class="plus">
            <i class="fas fa-plus-circle" v-bind:class="operationType"></i>
        </div>
    </div>
</template>

<script>
export default {
    name:'PriceRegulator' ,
    props: {
        operationType: String,
        price:Number
    }
}
</script>