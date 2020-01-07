<template>
  <div class="welcome">
    <h1>Welcome to the Name Service Web App</h1>
    <p>This is a web app meant to interact with the <a target="_blank" href="https://tutorials.cosmos.network/nameservice/tutorial/00-intro.html">Name Service</a> network that was built with the <a target="_blank" href="https://github.com/cosmos/cosmos-sdk">Cosmos-SDK</a>. This web app was built with <a target="_blank" href="https://github.com/vuejs/vue">Vue.js</a> and is being served by <a target="_blank" href="https://netlify.com">Netlify</a>. The code is on <a target="_blank" href="https://github.com/okwme/nameservice-webapp">Github</a>.</p>
    <p>The Name Service Network consists of a single node running on a <a target="_blank" href="https://digitalocean.com">Digital Ocean</a> server with a REST client accessible at <a target="_blank" href="https://node.talkshop.name/node_info">node.talkshop.name</a>. The Tendermint client is accessible at <a target="_blank" href="https://cli.talkshop.name">cli.talkshop.name</a>.</p>
    <hr>
    <p>This web app provides a few different sections meant to help you interact with the Name Service network:</p>
      
      <ol>
        <li><b>Commands</b> will tell you CLI commands to interact with the Name Service.</li>
        <li><b>Names</b> will display all the currently registered names.</li>
        <li><b>Faucet</b> will allow you to request some <i>nametoken</i> which can be used to create new names.</li>
      </ol> 
  </div>
</template>

<script>
export default {
  name: 'Welcome'
}
</script>

<style scoped>

</style>
