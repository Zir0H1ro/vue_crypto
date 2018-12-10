<template>
    <p>Enter amount:</p>
    <div class="currency-amount-select d-flex">
    <div class="currency-amount">
        <h6>0</h6>
        <p>{{currency}}</p>
    </div> 
        
    </div>
</template>

<script>
export default {
    name:'AmountRegulator',
    props:{
        currency:String,
        targetCurrency:String
    },
    data(){
        return{
            percentages:[
                '25%',
                '50%',
                '75%',
                '100%'
            ]
        }
    }
}