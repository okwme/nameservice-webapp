<template>
  <div id="app">
    <div id="corner">
      <span id="title">Name Service Web App</span>
      <ul>
        <li><a :class="view === 'welcome' ? 'active': 'inactive'" href="#" @click.prevent="view = 'welcome'">Welcome</a></li>
        <li><a :class="view === 'commands' ? 'active': 'inactive'" href="#" @click.prevent="view = 'commands'">Commands</a></li>
        <li><a :class="view === 'names' ? 'active': 'inactive'" href="#" @click.prevent="view = 'names'">Names</a></li>
        <li><a :class="view === 'faucet' ? 'active': 'inactive'" href="#" @click.prevent="view = 'faucet'">Faucet</a></li>
      </ul>
    </div>
    <div id="page">
      <Commands v-show="view === 'commands'"/>
      <Names v-show="view === 'names'"/>
      <Faucet v-show="view === 'faucet'"/>
      <Welcome v-show="view === 'welcome'" />
    </div>
  </div>
</template>

<script>
import Commands from './components/Commands.vue'
import Names from './components/Names.vue'
import Faucet from './components/Faucet.vue'
import Welcome from './components/Welcome.vue'

export default {
  name: 'app',
  data() {
    return  {
      view: "welcome"
    }
  },
  components: {
    Welcome,
    Commands,
    Names,
    Faucet,
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
body, html {
  padding:0;
  margin:0;
}
#title {
  font-weight: bold;
}
#corner {
  position: absolute;
  top:0px;
  left:0px;
  padding:10px;
  width: 100%;
  border-bottom: 1px solid black;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #494949;
  margin-top: 60px;
}
#page {
  max-width: 800px;
  margin:auto;
}
ul {
  display: inline;
}
ul li {
  display: inline;
  margin:5px;
}
ul li a {
  color: black;
  text-decoration: none;
}
ul li a.active {
  text-decoration: underline;
}
.center {
  text-align: center;
}
a {
  color: blue;
}
</style>
