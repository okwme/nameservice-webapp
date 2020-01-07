<template>
    <div class="commands">
        <div class="center">
            <input v-model="yourName" placeholder="YOUR_NAME"/>
            <input v-model="theirName" placeholder="THEIR_NAME"/>
            <input v-model="someDomain" placeholder="SOME_DOMAIN"/>
            <input v-model="someValue" placeholder="SOME_VALUE"/>
        </div>
        <pre id="textarea">
# create an account for yourself
nscli keys add {{yourName}}

# set your configs
nscli config chain-id namechain
nscli config node cli.talkshop.name:80
nscli config indent true
nscli config trust-node true

# query an account
nscli query account $(nscli keys show {{yourName}} --address)

# send some money
nscli tx send --amount 1nametoken \
--from $(nscli keys show {{yourName}} --address) \
--to $(nscli keys show {{theirName}} --address)

# buy a name!
nscli tx nameservice buy-name {{someDomain}} 5nametoken \
--from     $(nscli keys show {{yourName}} --address)

# set a resolver
nscli tx nameservice set-name {{someDomain}} {{someValue}}\
--from     $(nscli keys show {{yourName}} --address)

# resolve a name
nscli query nameservice resolve {{someDomain}}

# get the whole whois of a name
nscli query nameservice whois {{someDomain}}</pre>
    </div>
</template>

<script>
export default {
  name: 'Commands',
  data() {
      return {
          yourName: 'YOUR_NAME',
          theirName: 'THEIR_NAME',
          someValue: 'SOME_VALUE',
          someDomain: 'SOME_DOMAIN'
      }
  },
  computed: {
  }
}
</script>

<style scoped>
input {
    padding:1px 2px;
    margin:10px 5px;
    display:inline-block;
}
#textarea {
  text-align: left;
  width: 100%;
  /* max-width: 580px; */
  /* height: 400px; */
  font-size: 14px;
  font-family: monospace;
  padding: 20px;
  line-height: 1.4em;
  background-color: rgb(216, 216, 216);
  color: grey;
  border: 0px;
  white-space: pre-wrap;
  margin:auto;
}
</style>
