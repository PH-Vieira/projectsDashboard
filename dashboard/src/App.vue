<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <nav>
    <div class="navLeft">
      <button type="button" class="toggleBtn"></button>
      <img src="./assets/journal-bookmark-fill.svg" alt="bookmark fill" />
      <div class="title">Dashboard</div>
    </div>
    <div class="navRight">
      <button type="button" class="topBtn minimizeBtn"></button>
      <button type="button" class="topBtn maximizeBtn"></button>
      <button type="button" class="topBtn closeBtn"></button>
    </div>
  </nav>
  <router-view />
</template>

<style lang="scss">
@use "./style/colors";

body,
html {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: colors.$philippineOrange;
}

nav {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  width: 100%;
  height: 100%;
  border-bottom: 3px solid colors.$russianViolet;
  -webkit-user-select: none;

  .navLeft {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 100%;

    .toggleBtn {
      width: 48px;
      height: 40px;
      border: none;
      outline: none;
      background-color: transparent;
      background-repeat: no-repeat;
      background-position: center;
      transition: 0.2s;
      cursor: pointer;
      background-image: url("./assets/list.svg");
    }

    img {
      margin-left: 10px;
    }

    .title {
      margin: 10px 0 0 5px;
      width: 100%;
      line-height: 30px;
      padding-bottom: 5px;
      -webkit-app-region: drag;
    }
  }

  .navRight {
    display: flex;
    flex-direction: row;
    width: 120px;
    height: 40px;

    .topBtn {
      width: 48px;
      height: 40px;
      border: none;
      outline: none;
      background-color: transparent;
      background-repeat: no-repeat;
      background-position: center;
      transition: 0.2s;
      cursor: pointer;
    }

    .topBtn:hover {
      background-color: colors.$grape;
    }

    .topBtn:active {
      background-color: colors.$orangePeel;
    }

    .minimizeBtn {
      background-image: url("./assets/dash-lg.svg");
    }

    .maximizeBtn {
      background-image: url("./assets/copy.svg");
    }

    .closeBtn {
      background-image: url("./assets/x-lg.svg");
    }
  }
}

// nav {
//   padding: 30px;

//   a {
//     font-weight: bold;
//     color: colors.$russianViolet;

//     &.router-link-exact-active {
//       color: colors.$lavenderIndigo;
//     }
//   }
// }
</style>
