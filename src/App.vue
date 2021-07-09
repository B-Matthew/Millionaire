
<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      <div>
        <img src="./assets/millionaire.png" alt="">
      </div>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#nav {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 40vh;
  background: radial-gradient(circle,rgba(7,8,139,1) 9%, rgba(22,6,112,1) 71%);
}

#nav {
  padding: 30px;
  img {
    width: 15%;
    height: 15%;
    margin-top: 30px;
  }
  a {
    font-weight: bold;
    color: white;
    text-decoration: none;
    &:hover {
      color: greenyellow;
    }
  }
}

.home {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: #11093A;
  height: 60vh;
  text-align: center;
  .myContainer {
    width: 60%;
    margin: auto;
    color: white;
    ul {
      display: flex;
      flex-wrap: wrap;
      list-style-type: none;
      justify-content: space-around;
      li:first-child {
        flex-basis: 80%;
        margin: 60px 0;
      }
      li {
        flex-basis: 45%;
        border: 2px solid white;
        border-radius: 50%;
        padding: 30px 20px;
        margin: 30px 0;
      }
    }
  }
}
</style>
