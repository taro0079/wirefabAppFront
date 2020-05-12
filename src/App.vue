<template>
	<v-app>
		<div>
			<v-app-bar color="deep-purple accent-4" dense dark>
				<v-toolbar-title>Taro's Apps</v-toolbar-title>
				<v-spacer></v-spacer>
			</v-app-bar>
		</div>
	<router-view></router-view>

	<v-footer absolute class="font-weight-medium">
		<v-col class="text-center">			
			<router-link to="/">HOME</router-link>
			<div>
				{{ new Date().getFullYear() }} - <strong>Taro's Apps</strong>
			</div>		
		</v-col>
	</v-footer>
	</v-app>
  <!-- <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </div> -->
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
