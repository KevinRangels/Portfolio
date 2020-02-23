<template>
  <div class="home">
	<Billboard></Billboard>
  <PanelMain></PanelMain>
  </div>
</template>

<script>
// @ is an alias to /src
import Billboard from '@/components/Billboard.vue'
import PanelMain from '@/components/PanelMain.vue'


export default {
  name: 'home',
  components: {
    Billboard,
    PanelMain
  }
}
</script>
<style scoped>
	.home{
		background-color: black;
	}
</style>
