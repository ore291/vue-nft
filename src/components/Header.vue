<template>
  <div class="header">
    <div class="hlogo">
      <img src="@/assets/header/cryptopunk-logo.png" alt="crypto-punkHeader" />
    </div>
    <div class="searchBar">
      <div class="searchIconContainer">
        <img src="@/assets/header/search.png" alt="search" />
      </div>
      <input
        type="text"
        class="searchInput"
        placeholder="Collection, item or user ..."
      />
    </div>
    <div class="headerItems" v-for="(link, index) in links" :key="index">
      <p>{{ link.name }}</p>
    </div>
    <div class="headerActions">
      <div class="themeSwitchContainer">
        <img src="@/assets/header/theme-switch.png" alt="" />
      </div>
    </div>
    <div class="headerButton">
        <button>GET IN</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          name: "Drops",
          link: "#",
        },
        {
          name: "Marketplace",
          link: "#",
        },
        {
          name: "Create",
          link: "#",
        },
      ],
    };
  },
};
</script>

<style  scoped>
h2 {
  color: white;
}
.header {
  height: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.header > div {
  margin: 10px;
}

.hlogo > img {
  width: 200px;
}

.searchBar {
  background-color: #1c1c1e;
  display: flex;
  flex: 1;
  height: 50px;
  border-radius: 50px;
  align-items: center;
}
.searchIconContainer {
  margin: 10px;
}

.searchInput {
  background-color: transparent;
  border: none;
  width: 100%;
  outline: none;
  color: #eee;
  font-size: 16px;
}
.headerItems {
  color: white;
  display: flex;
}
.headerItems > p {
  margin: 10px;
}

.headerActions {
  display: flex;
  align-items: center;
}

.headerActions > div {
  margin: 10px;
}

.themeSwitchContainer{
    display: flex;
    background-color: #1c1c1e;
    border-radius: 100%;
    padding: 15px;
    justify-content: center;
    align-items: center;
    object-fit: contain;
}

.themeSwitchContainer > img{
    height: 25px;
}

.headerButton > button{
    background: linear-gradient(to right, #59f9b7, #4fab9f);
    border-radius: 50px;
    padding: 15px 40px;
    border: none;
    cursor: pointer;

}
</style>