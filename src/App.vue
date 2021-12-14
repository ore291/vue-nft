<template>
  <div id="app">
    <Header />
    <HeroContent :activePunk="punks[selectedPunk]"/>
    <CollectionList :punks='punks' @setActivePunk='setSelectedPunk'/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import CollectionList from "./components/CollectionList.vue";
import HeroContent from './components/HeroContent.vue'
import punks from '@/assets/data.json'


export default {
  name: "App",
  // mounted() {
  //   this.sendGetRequest();
  // },
  components: {
    Header,
    CollectionList,
    HeroContent
  },
  data() {
    return {
      selectedPunk: 0,
      punks: punks.assets,
    };
  },
  methods: {
    setSelectedPunk(e){
      this.selectedPunk = e;
    }
    // async sendGetRequest() {
    //   const URL = "https://testnets-api.opensea.io/assets?asset_contract_address=0x4C2e004AB5a84e936028aCF92cE6cb7815CEBb6f&order_direction=asc";
    //   const headers = {
    //           "Access-Control-Allow-Origin": "*",
    //           "Access-Control-Allow-Headers": "*",
    //           'Access-Control-Allow-Credentials' : 'true',
              
    //         }
    //   try {
    //     const resp = await this.axios.get(
    //       URL,
          
    //       {
    //         headers
    //       }
    //     );
    //     console.log(resp.data);
    //   } catch (err) {
    //     // Handle Error Here
    //     console.error(err);
    //   }
    // },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: black;
  padding: 20px;
  min-height: 100vh;
  max-width: 100vw;
}
</style>
