<template>
    <div class="header">
        <span>
            <div class="logo">
                <img src="../assets/doge.png">
            </div>
        </span>
        <span style="margin-left:5px">
            <div class="sign">
                <h1>Weather Search</h1>
            </div>
        </span>
        <span style="float:right">
            <div class="link">
                <a v-bind:href="url"><h1>More Project</h1></a>
            </div>
        </span>
    </div>
</template>
<script>
export default {
    name:'top',
    data(){
        return{
            url:'https://github.com/jackpot66663?tab=repositories'
        }
    }
}
</script>
<style scoped src="../assets/css/header.css">
</style>