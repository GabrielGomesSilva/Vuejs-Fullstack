<template>
  <div id="slogan"> 
      <div class="text-center">
          <h1> gabriel</h1>
          <br/>
          <h6 class="text-secondary"> Gerador de nomes ultilizando vue </h6>
      </div>
      <div id="main">
        <div class="container">
          <div class="row">
            <div class="col-md">
              <h5>prefixos <span class="badge badge-info">{{ prefixes.length }}</span> </h5>
              <div class="card">
                <div class="card-body">
                  <ul class="list-group">
                    <li class="list-group-item" v-for="prefix in prefixes" v-bind:key="prefix">
                      {{ prefix }}
                    </li>
                  </ul>
                  <br/>
                  <input class="form-control" type="text" placeholder="Digite o Prefixo">


                </div>
              </div>
            </div>
            <div class="col-md">
              <h5>sufixos <span class="badge badge-info">{{ prefixes.length }}</span></h5>
               <div class="card">
                <div class="card-body">
                  <ul class="list-group">
                    <li class="list-group-item" v-for="sufix in sufixes " v-bind:key= "sufix" >
                      {{sufix}}
                    </li>

                  </ul>
                  <br/>
                  <input class="form-control" type="text" placeholder="Digite o sufixo">

                </div>
              </div>

            </div>


          </div>
          <br/>
          <h5> Domínios <span class="badge badge-info"> {{ domains.length }} </span> </h5>

          <div class="card">
            <div class="card-body">
              <ul class="list-group">
                <li class="list-group-item" v-for="domain in domains" v-bind:key="domain.name">
                  {{domain}}


                </li>

              </ul>


            </div>


          </div>


        </div>
        
      </div>

  </div>
</template>

<script>

import "bootstrap/dist/css/bootstrap.css"
import "font-awesome/css/font-awesome.css"

export default {
  name: 'app',
 data: function(){
    return{
      prefixes:['air', 'jet', 'fligth'],
      sufixes:['hub','Station','Mart'],
      domains:['Airhub', 'AirStation', 'AirMart', 'jethub', 'jetStation','JetMart', 'FlightHub','FlighStation','Flighmart' ]

    };

 }


}



</script>

<style>

#slogan{

margin-top:30px;
margin-bottom:30px;


}

#main{
background-color: #f1f1f1;
padding-top:30px;
padding-bottom: 30px;


}




</style>
