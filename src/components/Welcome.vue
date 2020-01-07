<template>
  <div class="welcome">
    <h1>Welcome to the Cosmos-SDK Nameservice App</h1>
    <p>This is a webapp meant to interact with the <a href="https://tutorials.cosmos.network/nameservice/tutorial/00-intro.html">nameservice</a> decentralized app that was built with <a href="https://github.com/cosmos/cosmos-sdk">Cosmos-SDK</a>. This webapp was built with <a href="https://github.com/vuejs/vue">Vue.js</a>. The decentralized app consists of a single node running on a Digital Ocean server and accessible at <a href="https://node.talkshop.name/node_info">node.talkshop.name</a>. You can find the code on <a href="https://github.com/okwme/talkshop">github</a>.</p>
    <p>On this website you will find a few different sections meant to help you interact with the nameservice app in the following ways:</p>
      
      <ol>
        <li><b>Commands</b> will tell you CLI commands to interact with the nameservice.</li>
        <li><b>Names</b> will display all the currently registered names.</li>
        <li><b>Faucet</b> will allow you to request some <i>Nametoken</i> which can be used to create new names.</li>
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
