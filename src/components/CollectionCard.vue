<template>
  <div class="card">
    <img class="nftCollectionImg" :src="punk.image_original_url" :alt="punk.name" />
    <div class="details">
      <div class="name">
        {{ punk.name }}
        <div class="id">&middot; #{{ punk.token_id }}</div>
      </div>
      <div class="priceContainer">
        <img class="weth-img" src="@/assets/weth.png" alt="weth-img" />
        <div class="price">{{ punk.traits[0].value }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["punk"],
};
</script>

<style  scoped>
.card {
  color: white;
  background-color: #1a1c1e;
  border-radius: 20px;
  align-items: center;
  overflow: hidden;
  width: 300px;
  height: 500px;
  margin-right: 30px;
}
.nftCollectionImg {
  width: 100%;
}
.weth-img {
  height: 23px;
  width: 15px;
}
.details {
  padding: 20px;
}
.name {
  font-size: 20px;
  font-weight: 900;
}

.id {
  color: #a1a5b0;
  font-size: 18px;
  font-weight: 600;
}
.priceContainer {
  display: flex;
  align-items: center;
  object-fit: contain;
  margin-top: 10px;
}
.price {
  margin-left: 5px;
  font-weight: 600;
}
</style>