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
import axios from 'axios'

export default {
  name: 'home',
  components: {
    Billboard,
    PanelMain
  },
  data(){
    return {
      Digimon: []
    }
  },
  methods: {
    getDigimon(){
            axios.get('https://digimon-api.herokuapp.com/api/digimon')
            .then( res =>{ this.Digimon = res.data, console.log(this.Digimon) })
            
            .catch(err => console.log('Digimon', err));

          },
    filter(){
      this.Digimon =  this.Digimon.filter(digi => {
        return this.Digimon.level === "In Training"
        console.log(this.Digimon)
      })  
    } 
  },
  mounted () {
  }
}
</script>
<style scoped>
	.home{
		background-color: #000;
	}
</style>
