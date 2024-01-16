<template>
    <div class="header-container">
        <div class="title">
            <h1><span>Code</span>lândia</h1>
        </div>
        <div class="search">
            <input type="text" placeholder="Pesquisar no blog">
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>

.header-container{
    background: #17171A;
    padding:50px 0px;
}

h1{
    text-align: center;
    color: #FFF;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 40px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    margin-bottom:40px;
}

h1 span{
    color: #E07B67;
}

.search{
    display: flex;
    justify-content: center;
}

.search input{
    display: flex;
    padding: 16px 24px;
    align-items: center;
    gap: 16px;
    min-width: 1200px;
    border-radius: 8px;
    border: 2px solid #252529;
    background: #202024;
    color: #fff;
}

</style>