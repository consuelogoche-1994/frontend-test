<template>
    <div >
        <div class="itemMenu" :id="id">
            <div class="">{{product}}</div>
            <div class="itemMenu__price">{{price}}</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Itemmenu',
  data(){
      return{
      }
  },
  props: [
      'id',
      'product',
      'price'
  ]
}
</script>

<style scoped lang="scss">
.itemMenu{
    margin: 1rem;
    min-height: 4rem;
    width: auto;
    border-radius: 10px;
    color: black;
    font-weight: 600;
    background-color: #eeeeee;
    border:1px solid #ba68c8;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    padding: 0 2rem;
    font-size: 1.2rem;
    &__price{
        font-size: 1rem;
        font-weight: 500;
    }
    &:hover{
        cursor: pointer;
        background-color: #ba68c8;
        color:white;
    }
}
</style>