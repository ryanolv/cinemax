<template>
  <nav id="NavBar">
    <RouterLink to="/">
        <img src="/img/logo.png" alt="CineMax" id="logo">
    </RouterLink>
    <div>
        <!-- <router-link to="/">Cinemax</router-link>  -->
        <router-link to="/schedule">Programação</router-link>
    </div>
  </nav>
</template>

<script>
    export default {
        name: 'Navbar'
    }
</script>

<style scoped>
    #NavBar {
        padding: 15px 20px;
        background-color: #222;
        /* box-shadow: 60px -16px #888 ; */
        height: 60px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    #NavBar div {
        margin-right: 40px;
        backdrop-filter: blur(2px);
    }

    #NavBar div:hover {
        background-color: #6F0A0A;
        padding: 5px 10px;
        border-radius: 8px;
        transition: .5s;
    }

    #NavBar div a {
        text-decoration: none;
        color: #fff;
        font-weight: 400;
        font-size: 30px;
        line-height: 49px;
    }

    #NavBar div a:hover {
        /* font-weight: bold; */
    }
</style>