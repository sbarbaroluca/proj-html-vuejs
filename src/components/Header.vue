<template>
  <header>
    <div class="nav_menu">
        <ul class="inline_menu">
          <li>
            <i class="fas fa-home" id="home"></i>
          </li> 
          <li class="column_link" v-for="(n,index) in links.length/2" :key="index">
            <i :class="links[index].icon"></i>
          <div class="color">
            <a href="#">{{links[index].title}}</a>
            <p>{{links[index].subtitle}}</p>
          </div>
          </li>    
          <li>
          <img src="../assets/images/avada-spa-logo-new.png" alt="LogoNav">
          </li>
          <li class="column_link" v-for="(n,index) in links.length/2" :key="index">
            <i :class="links[index+links.length/2].icon"></i>
          <div class="color">
            <a href="#">{{links[index+links.length/2].title}}</a>
            <p>{{links[index+links.length/2].subtitle}}</p>
          </div>
          </li>    
          <li>  
            <i class="fas fa-plus" id="plus"></i>
          </li>  
        </ul>
      </div>
    

    <div class="jumbotron">
      <div class="text">
        <h2 class="title">Give yourself permission</h2>
        <h2 class="relax">Relax, Revive & Rejuvenate</h2>
        <div class="button">
          <p>EXPLORE TREATEMENTS</p>
        </div>
      </div>
    </div>
  </header>        
</template>

<script>
export default {
    name: "Header",
    props: {
      links: Array,
    }
}
</script>

<style lang="scss" scoped>
@import "~@fortawesome/fontawesome-free/css/all.css";
@import "~@fontsource/lato/700.css";
.nav_menu {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2;
  width: 100%;
  padding: 25px 30px;
  align-items: center;
  background-color: white;

  .inline_menu {
    display: flex;
    justify-content: space-around;
    align-items: center;
    list-style: none;

    .color {
      color: #70727b;
      font-family: Lato;;
      text-align: center;
    }
    .color a {
      font-size: 14px;
      text-transform: uppercase;
      font-weight: 700;
    }
    .color p {
      font-size: 11px;
    }

    .column_link {
      gap: 5px;
      display: flex;
      flex-direction: column;
      align-items: center;
      color: #b9afa1;
      cursor: pointer;
      &:hover {
      color: #33a7b9;
      }
    }
    

    li {
      display: inline-block;
      margin: 0 10px;

      a {
        text-decoration: none;
        color: currentColor;
        font-weight: 400;
        font-size: 12px;
        padding: 0 5px;
      }
      #home {
        color: #33a7b9;
      }
      #plus {
        color: #b9afa1;
      }
    }
  }
  .search {
    width: 25%;
    i {
      margin: 0 10px;
    }
    input {
      border: none;
      padding: 10px 60px 10px 10px;
      border-radius: 5px;
      background-color: #f5f5f5;
    }
    fa-search {
      position: relative;
      left: -35px;
      font-size: 12px;
      color: #36af96;
    }
  }
}

.jumbotron {
  position: relative;
  height: 937px;
  margin-top: 60px;
  background-image: url("../assets/images/avada-spa-slider-image-1-new.jpg");
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;


  .text {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    font-family: libre-baskerville;
    color: white;
    .title {
      font-size: 40px;
      font-weight: 400;
      margin: 5px;
      font-style: italic;
      color: #f0e5d7;
    }
    .relax {
      font-size: 90px;
      font-weight: 400;
      text-align: center;
      
    }
    .button {
      font-family: Lato;
      font-style: normal;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 15px 40px;
      margin-top: 50px;
      border-radius: 50px;
      text-align: center;
      font-size: 14px;
      background-color:#b9afa1;;
      color: white;
      transition: all 0.2s ease;
      p {
        display: inline-block;
        margin-right: 10px;
      }
      i {
        font-size: 12px;
      }
      &:hover {
        cursor: pointer;
        color: white;
        background-color: #33a7b9;
      }
    }
  }
}
</style>