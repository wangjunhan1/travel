<template>
	<div id="app">
        <tab></tab>
        <router-view />
	</div>
</template>

<script>
    import Tab from './pages/tab/tab'

    export default {
      name: 'App',
      components: {
        Tab
      }
    }
</script>

<style>

</style>
