<template>
  <div class="home">
      <div class="row">
        <div class="col s6">
          <div class="col s6">
            <a class="col s12 waves-effect waves-light btn purple lighten" v-on:click="menuSelect = menu.breakfast" >Desayuno</a>
          </div>
          <div class="col s6">
           <a class="col s12 waves-effect waves-light btn  purple lighten-2" v-on:click="menuSelect = menu.otherCat">Resto del día</a>
          </div>
        </div>
        <div class="col s6">
          Resumen de pedido
        </div>
      </div>
      <div class="row">
        <div class="col s6 sectionContainer">
          <Itemmenu v-for="(item,key) in  menuSelect" :key="key" :id="item.id" :product="item.product" :price="item.price"></Itemmenu>
        </div>
        <div class="col s6 sectionContainer">
        </div>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import Itemmenu from '@/components/Itemmenu.vue';

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Itemmenu
  },
  data(){
    return{
      menu : {
          breakfast:[
          { id:1 , product:'Café americano', price:5 },
          { id:2 ,product:'Café con leche', price:7 },
          { id:3 ,product:'Sandwich de jamón y queso', price:10 },
          { id:4 ,product:'Jugo de frutas natural', price:7 },
          ],
          otherCat:[
          { id:5 ,product:'Hamburguesa simple', price:10 },
          { id:6 ,product:'Hamburguesa doble', price:	15 },
          { id:7 ,product:'Papas fritas', price:5 },
          { id:8 ,product:'Aros de cebolla', price:5 },
          { id:9 ,product:'Agua 500ml', price:5 },
          { id:10 ,product:'Agua 750ml', price:5 },
          { id:11 ,product:'Bebida/gaseosa 500ml', price:7 },
          { id:12 ,product:'Bebida/gaseosa 750ml', price:10 },
          ]
      },
      menuSelect:[],
    }
  },
  methods: {
  },
}
</script>

<style lang="scss">
  .sectionContainer{
    border-radius: 5px;
    border:2px solid #ab47bc;
    display: flex;
    justify-content: flex-start;
    flex-flow: row wrap;
  }
</style>
