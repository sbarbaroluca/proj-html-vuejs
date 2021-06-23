<template>
 <footer>
   <div class="foot">
     <img src="../assets/images/avada-spa-logo-new.png" alt="logo-footer">
   </div>
   <div class="testo">  
      <p class="copyright">© Copyright 2016 | Avada Theme by<span class="green"> ThemeFusion</span> | All Rights Reserved | Powered by <span>WordPress</span></p>
   </div>   
   <div class="social">
     <a href="#" :class="social.icon" v-for="(social,index) in socials" :key="index"></a>
   </div>
 </footer>
</template>

<script>
export default {
      name: "Footer",
    props: {
      socials: Array,
    }
}
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 35px;
}
.testo {
  max-width: 400px;
}
p {
  font-family: Lato;
  text-align: center;
  font-size: 13px;
  color: rgba(68,64,90,0.6);
}
span {
  color: #b9afa1;
  cursor: pointer;
  &:hover {
      color: #a0a4b1;
      }
}
a {
  color: #BEBDBD;
  font-size: 20px;
  padding: 12px;
  margin: 5px;
  background-color: #e9e9e9;
  border-color: #e9e9e9;
  border-radius: 4px;
  text-decoration: none;
}
</style>