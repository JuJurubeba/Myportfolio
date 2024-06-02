<template>
  <header>
    <div class="interface">
      <div class="logo">
          <a href="#"><img src="../assets/logo.png" alt=""></a>
      </div>
      <nav class="menu-desktop">
          <ul>
              <li><a href="#">inicio</a></li>
              <li><a href="#">Sobre</a></li>
              <li><a href="#">Projetos</a></li>
          </ul>
      </nav>

      <div class="btn-contato">
          <a href="#">
              <button>Contato</button>
          </a>
      </div>
      <div class="btn-abrir-menu" id="btn-menu">
        <img src="../assets/list.svg" alt="" h>
      </div>
      <div class="menu-mobile" id="menu-mobile">
        <div class="btn-fechar">
          <i class="bi bi-x-lg">x</i>
        </div>
        <nav>
          <ul>
              <li><a href="#">inicio</a></li>
              <li><a href="#">Sobre</a></li>
              <li><a href="#">Projetos</a></li>
              <li><a href="#">Contato </a></li>
          </ul>
      </nav>
    
      </div>
      <div class="overlay-menu" id="overlay-menu"></div>
  </div>
  
    

  </header>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    let btnMenu = document.getElementById('btn-menu')
    let menu = document.getElementById('menu-mobile')
    let overlay = document.getElementById('overlay-menu')

    btnMenu.addEventListener('click',()=>{
      menu.classList.add('abrir-menu')
    })
    menu.addEventListener('click',()=>{
      menu.classList.remove('abrir-menu')
    })
    overlay.addEventListener('click',()=>{
      menu.classList.remove('abrir-menu')
    })


  }
}

</script>


<style scoped>
header{
  padding: 25px 4%;
  margin-left: 0%;
  
}
/*menu mobile*/
.btn-abrir-menu{
  display: none; 
}
.menu-mobile{
 display: none;
}
.overlay-menu{
  display: none;
}



header > .interface{
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  padding: 60px 4%;
  
}
header a{
  color: #5c5c5c;
  text-decoration: none;
  display: inline-block;
}
header nav.menu-desktop a:hover{
  color: white;
  transform: scale(1.05);

}
header nav ul{
  list-style-type: none;
  

}
header nav.menu-desktop ul li {
  display: inline-block;
  padding: 0 40px;
  
}
/* Estilod o topo do site*/
button:hover{
  box-shadow: 0px 0px 10px #7ffef5;
  transform: scale(1.05);
}
@media screen and (max-width: 1020px) {
  .menu-desktop, .btn-contato{
    display: none;
  }
  .menu-mobile{
    background-color:  #000;;
    height: 100vh;
    position: fixed;
    top: 0;
    right: 0;
    z-index: 999999;
    width: 0%;
    overflow: hidden;
    transition: .5s;
    visibility: visible;
  }
  .menu-mobile nav ul{
    text-align: right;
  }
  .menu-mobile nav ul li a{
    color: white;
    font-size: 20px;
    font-weight: 300;
    padding: 20px 8%;
    display: block;
  }
  .menu-mobile nav ul li a:hover{
    background-color:#7ffef5 ;
    color: black;
  }
  .menu-mobile .btn-fechar i{
    color:#7ffef5;
  }
  .menu-mobile .btn-fechar{
    padding: 20px 5%;
    font-size: 30px;
  }
  .btn-abrir-menu img{
      width: 40px;
      height: 40px;
      border-radius: 50%;
      border: none;
      background-color: #7ffef5;
      font-size: 22px;
      cursor: pointer;
      margin: 0 5px;
      visibility: visible;
  }
  .overlay-menu{
    background-color: #0000007c;
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0%;
    z-index: 88888;
    display: none;
  }
  .menu-mobile.abrir-menu{
    width: 70%;
  }
  .menu-mobile.abrir-menu ~ .overlay-menu{
    display: block;
  }
  .btn-abrir-menu{
    display: block;
    
  }
  .menu-mobile{
   display: block;
  }
  
  
  
}

</style>
