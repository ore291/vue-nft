<template>

  <div>
    
    <div class="list">
    <div @click="setSelectedPunk(punk.token_id)" v-for="punk in punks" :key="punk.token_id">
      <CollectionCard  :punk="punk" />
    </div>
    
  </div>
  </div>
</template>

<script>
import CollectionCard from "./CollectionCard.vue";

export default {
  components: {
    CollectionCard,
  },
  props: ['punks',],
  methods: {
    setSelectedPunk(id){
      this.$emit('setActivePunk', id)
    }
  },
  data() {
      return {
        
          // punk: {
          //     name: 'gecko',
          //     id: 0,
          //     traits: [{
          //         value: 7
          //     }],
          //     img: 'https://lh3.googleusercontent.com/m-Ws730SPYfr1hhPi44UWd923AthhSYnetE8x32yJf1b4GPOTOwdsgK9yXN7naVm7Y884R7e7yTxzMjDGfwpZaRQmfgA4Zo5CXy_jg=w294'
          // }
      }
  },
};
</script>

<style >
  .list{
    display: flex;
    justify-content: space-between;
    cursor: pointer;
    overflow: scroll;
    margin-top: 20px;
    padding-bottom: 20px;
    border-bottom: 1px solid white;

  }

  .list::-webkit-scrollbar {
    display: none;
  }
</style>