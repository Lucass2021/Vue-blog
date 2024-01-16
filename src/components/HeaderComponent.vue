<template>
    <div class="header-container">
        <div class="title">
            <h1><span>Code</span>land</h1>
        </div>
        <div class="search">
            <div>
                <button>
                    <font-awesome-icon class="searchIcon" :icon="['fas', 'search']"/>
                </button>
                <input type="text" placeholder="Search for a post">
            </div>
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

.search div{
    position: relative;
}

.search button{
    background: none;
    border:none;
    padding:16px;
    position: absolute;
    left: 0px;
    cursor:pointer;
}

.search .searchIcon{
    color: #E07B67;
    width: 16px;
    height: 16px;
}

.search input{
    display: flex;
    padding: 16px 24px;
    padding-left: 50px;
    align-items: center;
    gap: 16px;
    min-width: 1200px;
    border-radius: 8px;
    border: 2px solid #252529;
    background: #202024;
    color: #fff;
}

</style>