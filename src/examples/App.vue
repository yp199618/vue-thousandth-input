<template>
  <div id="app">
    <thousandth
      v-model="value"
			@change="change"
			@blur="blur"
			@focus="focus"
            @change_="change_"
			:decimalPoint="3"
			id-set="woshi"
    />

    <h5><br>Value is: {{ value }}</h5>

    <input v-model="value"/>
  </div>
</template>

<script>
import thousandth from './../components/thousandth.vue'

export default {
  name: 'App',
  components: {
    thousandth
  },
  data () {
    return {
      value: ''
    }
	},
	methods: {
        change_(){
            console.log('change_====',this.value)
        },
		change (obj) {
			console.log(obj, 'change');
		},
		blur (obj) {
			console.log(obj,'blur');
		},
		focus (obj) {
			console.log(obj,'focus');
		}
	}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
