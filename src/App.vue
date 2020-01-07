<template>
  <div id="app">
    <ul>
      <li><a :class="view === 'welcome' ? 'active': 'inactive'" href="#" @click.prevent="view = 'welcome'">Welcome</a></li>
      <li><a :class="view === 'commands' ? 'active': 'inactive'" href="#" @click.prevent="view = 'commands'">Commands</a></li>
      <li><a :class="view === 'names' ? 'active': 'inactive'" href="#" @click.prevent="view = 'names'">Names</a></li>
      <li><a :class="view === 'faucet' ? 'active': 'inactive'" href="#" @click.prevent="view = 'faucet'">Faucet</a></li>
    </ul>
    <div id="page">
      <Commands v-if="view === 'commands'"/>
      <Names v-else-if="view === 'names'"/>
      <Faucet v-else-if="view === 'faucet'"/>
      <Welcome v-else />
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
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
#page {
  max-width: 800px;
  margin:auto;
}
ul {
  text-align: center;
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
</style>
