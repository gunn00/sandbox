<template>
  <div>
    <nav class="nav-bar">
      <h2>
      <router-link 
      id="nav-bar-home"
      :to=" { name: 'home' }"
      >Home</router-link>
    </h2>
      <h2       id="nav-bar-book">Book</h2>
      <div id="nav-bar-book-items">
        <router-link :to=" {name: 'about'}">Book</router-link>
        <router-link :to=" {name: 'about'}">Book</router-link>
      </div>
      <h2 
      id="nav-bar-login">Login</h2>
    </nav>
    <router-view/>
  </div>
</template>

<script> 

export default {

  methods: {
    toggleDropdown(){
      document.getElementById("nav-bar-book-items").classList.toggle('.show')
    }
  }

}

</script>

<style scoped>
    @media only screen 
  and (min-device-width: 375px) 
  and (max-device-width: 812px) 
   { 
    .nav-bar{
      display: flex;
      justify-content: space-around;
      background-color: rgb(247, 218, 138);

    }

    .nav-bar > h2 {
      color: rgb(97, 151, 223);
      font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif ;
      display: block;
      font-weight: bold;
      margin-block-start: 0px;
      margin-block-end: 0px;
      padding: 10px;

    }

    .nav-bar > h2:hover{
      background: rgba(253, 180, 220, .5);
      
    }

    #nav-bar-home{
      text-decoration: none;
      color: rgb(97, 151, 223);
      font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif ;
      font-weight: bold;
      font-size: 25px;
    }
    
    #nav-bar-book-items{
      display: none;
    }

    .show{
      display: inline-flex;
    }
  }

</style>
