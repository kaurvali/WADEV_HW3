<template>
  <div class="wrapper">
    <div class="header">
      <div class="logo">
        <a href="/"><img src="../assets/logo.png" alt="PostIt" /></a>
      </div>
      <div class="search">
        <form><input type="text" /><button>Search</button></form>
        <Navigation />
      </div>
      <div class="user-control">
        <a id="account"
          ><img src="../assets/account.png" alt="Account Photo"
        /></a>
      </div>
    </div>
  </div>
</template>

<script>
import Navigation from "@/components/Navigation.vue";

export default {
  name: "Header",
  props: {},
  components: {
    Navigation,
  },
};
</script>

<style scoped lang="scss">
.wrapper {
  padding: 10px;
  top: 0;

  .header {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    align-items: center;

    .search {
      width: 40%;

      form > input {
        box-sizing: border-box;
        height: 35px;
        width: 75%;
        margin: 0;
        padding: 5px;
        border: 1px solid #e0e0e0;
      }
      form > button {
        box-sizing: border-box;
        height: 35px;
        width: 25%;
        margin: 0;
        padding: 5px;
        border: 1px solid #e0e0e0;
        cursor: pointer;
        background-color: #42b983;
        color: white;
        font-weight: 600;
      }
      form > button:hover {
        transition-duration: 0.5s;
        border: 1px solid #42b983;
        color: #42b983;
        background-color: white;
      }
    }

    #account img,
    .logo img {
      height: 40px;
      width: auto;
    }
  }
}
</style>
