<template>
    <header class=header>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    </header>
</template>

<script>
export default {
    name:"header"
}
</script>

<style scoped>
    .header{
        background: #333;
        color:#fff;
        text-align: center;
        padding: 10px;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        height: 100px;
    }

    .header a{
        text-decoration: none;
        padding-right: 5px;
        color: #fff;
    }
</style>