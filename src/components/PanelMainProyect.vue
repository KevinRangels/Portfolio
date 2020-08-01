<template>
  <div class="panelmain">
    <div class="panelmain_control">
      <div class="panelmain_container_perfil_img">
        <div class="panelmain_perfil_img"></div>
        <div class="panelmain_perfil_name">
          <h1 class="panelmain_name">Kevin Rangel</h1>
        </div>
      </div>
      <div class="panelmain_container_info">
        <div class="pannelmain_info_title">
          <h2 v-if="information == 1">Información Personal</h2>
          <h2 v-if="information == 2">Tecnologias</h2>
          <h2 v-if="information == 3">Proyectos</h2>
        </div>
        <div class="panelmain_info_text">
          <p v-if="information == 1">Sección que da a conocer información relevante a mi persona</p>
          <p v-if="information == 2">Esta sección muestra cuáles son las herramientas y técnicas que he usado en distintas tecnologías a la hora del desarrollo</p>
          <p v-if="information == 3">Esta sección da a conocer los proyectos que he realizado y tecnologías utilizadas en estos</p>
        </div>
      </div>
      <div class="panelmain_container_btns">
        <div @click="changueInformation_1" class="panelmain_btn" v-bind:class="[{ panelmain_active: information == 1 }]">
          <i class="fa fa-user panelmain_btn_icon"></i>
        </div>
        <div @click="changueInformation_2" class="panelmain_btn" v-bind:class="[{ panelmain_active: information == 2 }]">
          <i class="fas fa-briefcase panelmain_btn_icon"></i>
        </div>
        <div @click="changueInformation_3" class="panelmain_btn" v-bind:class="[{ panelmain_active: information == 3 }]">
          <i class="fas fa-suitcase panelmain_btn_icon"></i>
        </div>
      </div> 
    </div>

    <div class="panelmain_information">
      <div class="example-3d">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>

      </swiper-slide>
      <swiper-slide></swiper-slide>
      <swiper-slide></swiper-slide>
      <swiper-slide>Slide 4</swiper-slide>
      <swiper-slide>Slide 5</swiper-slide>
      <swiper-slide>Slide 6</swiper-slide>
      <swiper-slide>Slide 7</swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
    </div>
    
  </div>
</template>

<script>
// import NavHeader from '@/components/NavHeader.vue'
export default {
  name: 'PanelMainProyect',
  components: {

  },
  props: {
    msg: String
  },
  data(){
    return {
      information: 0,
     swiperOption: {

       effect: 'coverflow',
      grabCursor: true,
      centeredSlides: true,
      slidesPerView: 'auto',
      initialSlide: 1,
      coverflowEffect: {
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
      },
      pagination: {
        el: '.swiper-pagination',
      },
        
      },
    }
  },
  methods:{
    changueInformation_1(){
      this.information = 1;
    },
    changueInformation_2(){
      this.information = 2;
    },
    changueInformation_3(){
      this.information = 3;
    }
  }
}
</script>

<style scoped>

 .swiper-container {
      width: 100%;
      padding-top: 50px;
      padding-bottom: 50px;
    }

    .swiper-slide {
      background-position: center;
      background-size: cover;
      width: 300px;
      height: 300px;
      background: red

    }
	.panelmain{
    widows: 100%;
    height: 100vh;
    display: flex;
  }
  .panelmain_control{
    width: 30%;
    height: 100%;
    border-radius: 24px;
    background: black;
    border: 3px solid gold;
    overflow: hidden;
  }
  .panelmain_container_perfil_img{
    width: 100%;
    height: 40%;
    border: 1px solid red;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }
  .panelmain_perfil_img{
    border: 2px solid gold;
    width: 60%;
    height: 60%;
    border-radius: 50%;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 10px;
  }
  .panelmain_name{
    color: white;
  }
  .panelmain_container_info{
    height: 53%;
    border: 1px solid blue;
    padding-top: 14%;
    padding-bottom: 4%;
  }
  .pannelmain_info_title{
    color: gold;
  }
  .panelmain_info_text{
    color: white;
    padding-left: 3%;
    padding-right: 3%;
    font-size: 1.3rem;
  }






  .panelmain_container_btns{
    height: 7%;
    background: gold;
    display: flex;
  }
  .panelmain_btn{
    width: 100%;
    height: 100%;
    border: 1px solid gold;
    background: black;
    text-align: center;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-bottom: none;
  }
  .panelmain_btn_icon{
    font-size: 2rem;
    color: white;
  }
  .panelmain_active{
    background: gold;
  }







  .panelmain_information{
    border: 3px solid gold;
    width: 70%;
    height: 100%;
    display: flex;
    flex-direction: column;
    text-align: left;
    background: black;
    border-radius: 30px;
  }
  .panel_information_proyects{
    padding: 20px;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    overflow-y: auto;
  }
  .info1_container_description{
    margin-bottom: 20px;
    width: 50%;
  }
  

</style>
