<template>
  <div id="app">
    <Header 
    :links="headerlinks"
    />
    <Main />
    <Footer 
    :socials="socialLinks"
    />
  </div>
</template>

<script>
import Header from "./components/Header";
import Main from "./components/Main";
import Footer from "./components/Footer"
export default {
  name: 'App',
  components: {
        Header,
        Main,
        Footer
  },
  data() {
    return {
      headerlinks:[{
        title:"treatments", 
        icon:"fab fa-pagelines",
        subtitle:"Face & Body",
        },
        {
        title:"about", 
        icon:"fas fa-male",
        subtitle:"Our Team",
        },
        {
        title:"journal", 
        icon:"fas fa-heart",
        subtitle:"Tips & Triks",
        },
        {
        title:"book now", 
        icon:"fas fa-bookmark",
        subtitle:"Special Offers",
        }
        ],
      socialLinks:[{
        icon:"fab fa-facebook-square",
        title:"Facebook",
        },
        {
        icon:"fab fa-twitter",
        title:"Twitter",
        },
        {
        icon:"fab fa-instagram",
        title:"Instagram",
        },
        {
        icon:"fab fa-youtube",
        title:"Youtube",
        }
        ]
    }
  },
}

</script>

<style lang="scss">
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
