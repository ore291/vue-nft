<template>
  <div class="main">
    <div class="mainContent">
      <div class="heroImage">
        <div class="heroContainer">
          <img :src="activePunk.image_original_url" alt="" />
        </div>
      </div>
      <div class="heroDetails">
        <div class="title">
          {{ activePunk.name }}
          <span class="itemNumber"> &middot; #{{ activePunk.token_id }} </span>
        </div>

        <div class="owner">
          <div class="ownerImage">
            <img :src="activePunk.owner.profile_img_url" alt="" />
          </div>
          <div class="ownerDetails">
            <div class="ownerNameandHandle">
              <div class="ownerAddress">{{ activePunk.owner.address }}</div>
              <div class="ownerHandle">@knightLabs</div>
            </div>
            <div class="ownerLink">
              <img src="@/assets/owner/instagram.png" alt="" />
            </div>
            <div class="ownerLink">
              <img src="@/assets/owner/twitter.png" alt="" />
            </div>
            <div class="ownerLink">
              <img src="@/assets/owner/more.png" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["activePunk"],
};
</script>

<style>
.main {
  max-height: 50vh;
  color: white;
}
.mainContent {
  display: flex;
  padding-bottom: 20px;
  border-bottom: 1px solid white;
}

.heroImage {
  flex: 0.25;
  display: flex;
  align-items: center;
  justify-content: center;
}
.heroContainer {
  border-radius: 20px;
  overflow: hidden;
  display: flex;

  margin-right: 20px;
}
.heroDetails {
  display: flex;
  justify-content: space-between;
  flex: 0.75;
  flex-direction: column;
}

.heroContainer > img {
  object-fit: contain;
  max-width: min(30vw, 40vh);
  max-height: 30vw;
}

.title {
  font-size: 96px;
  font-weight: 800;
}

.itemNumber {
  color: #a1a5b0;
  font-size: 72px;
  align-self: center;
}

.owner {
  display: flex;
  margin: 10px 0;
  height: 50px;
}

.owner > div {
  margin: 0 5px;
}

.ownerImage {
  height: 50px;
  width: 50px;
  border-radius: 50%;
  border-radius: 50px;
  overflow: hidden;
  object-fit: contain;
}

.ownerImage > img {
  height: 100%;
  width: 100%;
}

.ownerDetails {
  display: flex;
  align-items: center;
  flex: 1;
}

.ownerNameandHandle {
  flex: 1;
}
.ownerHandle {
  color: #00e0fe;
}
.ownerLink {
  padding: 12px;
  border-radius: 50px;
  height: 50px;
  width: 50px;
  border: 1px solid white;
  margin: 0 0 0 10px;
}

.ownerLink > img {
  height: 100%;
  width: 100%;
}
</style>