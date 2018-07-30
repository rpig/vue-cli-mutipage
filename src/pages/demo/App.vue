<template>
  <div id="app">
    <img src="assetsogo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    async test() {
      const { a } = await this.aa();
      window.console.log(a);
      window.console.log('1111111');
      Object.assign({}, { a: 1 });
    },
    aa() {
      return new Promise((resolve) => {
        resolve();
        window.console.log('2222222');
      });
    },
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
