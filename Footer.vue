<template>
    <div class="footer">
        <div class="row">
            <div class="col-sm-2">
                <div class="title">Contact</div>
                <div class="icon">
                    <font-awesome-icon icon="phone"/>  09791429120
                </div>
                <div class="icon">
                    <font-awesome-icon icon="envelope"/>  superjack870610dd@gmail.com
                </div>
            </div>
            <div class="col-sm-2">
                <div class="title">Social</div>
                <div class="social-icon">
                    <a href="https://www.facebook.com/profile.php?id=100003466923371"><font-awesome-icon :icon="['fab', 'facebook']" style="color:black;" size="3x"/></a>
                </div>
                <div class="social-icon">
                    <a href="https://www.instagram.com/jackpot_610/?hl=zh-tw"><font-awesome-icon :icon="['fab', 'instagram']" style="color:black;" size="3x"/></a>
                </div>
            </div>
            <div class="col-sm-2">
                <div class="title">Portfolio</div>
                <div class="port-icon">
                    <a href="https://github.com/jackpot66663?tab=repositories"><font-awesome-icon :icon="['fab', 'github']" style="color:black;" size="3x"/></a>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped src="../assets/css/footer.css">
</style>
<script>
export default {
    name:'bottom'
}
</script>