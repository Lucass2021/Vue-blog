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
    padding:3.125rem 0rem;
}

h1{
    text-align: center;
    color: #FFF;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 2.5rem;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    margin-bottom:2.5rem;
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
    padding:1rem;
    position: absolute;
    left: 0rem;
    cursor:pointer;
}

.search .searchIcon{
    color: #E07B67;
    width: 1rem;
    height: 1rem;
}

.search input{
    display: flex;
    padding: 1rem 1.5rem;
    padding-left: 3.125rem;
    align-items: center;
    gap: 1rem;
    width: 75rem;
    border-radius: 0.5rem;
    border: 0.125rem solid #252529;
    background: #202024;
    color: #fff;
}


@media only screen and (max-width: 1400px) {
    .search input{
        width: 50rem;
    }
}

@media only screen and (max-width: 1000px) {
    .search input{
        width: 37.5rem;
    }
}

@media only screen and (max-width: 768px) {
    .search input{
        width: 31.25rem;
    }
}

@media only screen and (max-width: 568px) {
    .search input{
        width: 18.75rem;
    }
}

</style>