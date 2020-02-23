<template>
  <div class="nav_header pr-4">
    <div class="nav_header_container mt-1">
      <ul class="m-0" style="list-style: none; display: flex; justify-content: space-between;">
        
        <li class="nav_header_btn item tres">
          <a href="https://www.instagram.com/kevinrangels/"  target="_blank">
            <i class="fab fa-instagram lead  text-white" aria-hidden="true"></i>
          </a>
        </li>

        <li class="nav_header_btn">
          <a href="https://www.facebook.com/kevin.rangels" target="_blank" >
            <i class="fab fa-facebook-f  text-white" aria-hidden="true"></i>
          </a>
        </li>

        <li class="nav_header_btn">
          <a href="https://github.com/KevinRangels" target="_blank" >
            <i class="fab fa-github  text-white " aria-hidden="true"></i>
          </a>
        </li>
        <li class="text-white ml-4 mt-2">
          <a href="" class="header_menu_btn_lenguage">es</a> <span class="nav_header_btn_lenguage_div">|</span><a href="" class="header_menu_btn_lenguage">en</a>
        </li>

      </ul>      
    </div>

  </div>
</template>

<script>
export default {
  name: 'NavHeader',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .nav_header{
    height: 60px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .nav_header_container{
    display: flex;
    justify-content: flex-end;
  }
  .nav_header_btn{
    border: 2px solid white;
    width: 45px;
    text-align: center;
    display: flex;
    justify-content: center;
    margin-right: 10px;
    margin-left: 10px;
    padding: 7px;
    border-radius: 198px 198px 198px 198px;
  }
  .nav_header_btn a i .fab.fa-instagram{
  }
  .nav_header_btn a i .fab.fa-facebook-f{
  }
  .nav_header_btn a i .fab.fa-github{
  }
  .nav_header_btn a i{
    font-size: 26px;
  }
  .nav_header_btn a {
    margin-left: 5px;
    margin-right: 5px;
    margin-bottom: -1px;
  }
  .header_menu_btn_lenguage{
    color: white;
    text-decoration: none;
    font-weight: bold;
    font-size: 18px;
  }
  .nav_header_btn_lenguage_div{
    margin-right: 5px;
    font-size: 18px;
    font-weight: bold;
  }


/*  .item {
  background-color: rgba(0,0,0,0.4);
  line-height: 4;
  padding: 0 2em;
  margin:1.5em;
  color: #fff;
  position: relative;
}*/

.item:before {
  
  
  transition: all .3s;
}

.item:hover:before {
  border: 2px solid gold;
}

.tres:before {
  left: 50%;
}
.tres:hover:before {
  left:0;
}
</style>
