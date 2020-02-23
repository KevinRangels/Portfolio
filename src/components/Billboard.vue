<template>
  <div class="billboard">
    <NavHeader></NavHeader>
    <div class="billboard_container">
      <div class="container_main_title">
        <div class="container_title_detail animated fadeInLeft delay-3s" >
          <span class="billboard_title_detail"><</span>
        </div>
        <div class="container_title animated fadeIn delay-2s">
          <h1 class="billboard_title">Kevin Rangel</h1>
          <h2 class="billboard_subtitle animated fadeIn delay-3s">Desarrollador Web</h2>

        </div>
        <div class="container_title_detail animated fadeInRight delay-3s">
          <span class="billboard_title_detail">/></span>
        </div>
      </div>

    </div>
       <div class="billboard_container_arrow"> 
        <i class="fas fa-angle-down billboard_arrow animated bounce infinite delay-3s"></i>
      </div>
  </div>
</template>

<script>
import NavHeader from '@/components/NavHeader.vue'


export default {
  name: 'Billboard',
  components: {
    NavHeader
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
	.billboard{
		height: 100vh;
		background-color: black;
	}
  .billboard_container{
    border: 1px solid red;
    height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .container_main_title{
    border: 1px solid red;
    display: flex;
    justify-content: center;
  }
  .container_title{
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-top: 50px;
    padding-left: 20px;
    padding-right: 20px;
  }
  .billboard_title{
    font-size: 90px;
    color: white;
  }
  .container_title_detail{
    border: 1px solid red;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .billboard_title_detail{
    font-size: 180px;
    color: gold;
  }
  .billboard_container_arrow{
    border: 1px solid red;
    display: flex;
    justify-content: center;
  }
  .billboard_subtitle{
    color: white;
  }
  .billboard_arrow{
    font-size: 90px;
    color: white;
    cursor: pointer;
  }
</style>
