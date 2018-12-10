<template>
    <div class="top-bar d-flex">
        <div class="dx-logo col-1">
            <div class="red"></div>
            <div class="green"></div>
            <div class="blue"></div>
        </div>
        <h1>DX</h1>
        <div class="fund-management d-flex col-6">
            <div class="funds d-flex col-2">
                <span>Funds</span>
                <div class="fa-wrapper">
                    <i class="fa fa-caret-down"></i>
                </div>
            </div>
            <div class="values d-flex col-5">
                <div v-for="val in values" v-bind:key="val">
                    <p>{{val.name}}</p>
                    <h4 v-bind:class="val.classes">{{val.value}}</h4>
                </div>
                <div class="fa-wrapper">
                    <i class="fa fa-caret-down"></i>
                </div>
            </div>
            <div class="user-data col-4 d-flex">
                <div class="d-flex col-6">
                    <div>
                        <h4>{{name}}</h4>
                        <div class="time-data d-flex">
                            <p>{{hour}}</p>
                            <p>{{date}}</p>
                        </div>
                    </div>
                    <div class="fa-wrapper">
                        <i class="fa fa-caret-down"></i>
                    </div>
                </div>
                <div class="country-flag col-6">
                    <img v-bind:src="countryImg" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>


export default {
  name: 'TopBar',
  data(){
      return {
          name:'daniel daniel',
          hour:'09:54:40',
          date:'aug 11, 2017',
          countryImg:'UK-Union-flag.png',
          values:[
              {
                  'name':'Usd Value',
                  'value':'$21,000',
                  'classes':{

                  }
              },
              {
                  'name':'cfd margin',
                  'value':'$18,000',
                  'classes':{
                      
                  }
              },
              {
                  'name':'p&l',
                  'value':'$2,000',
                  'classes':{
                      'buy':true
                  }
              },
              {
                  'name':'available to trade',
                  'value':'$3,000',
                  'classes':{
                      
                  }
              }
          ]
      };
  }
}

</script>