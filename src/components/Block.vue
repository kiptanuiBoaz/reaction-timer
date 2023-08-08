<template>
    <div class="block" v-if="showBlock">
        Click ME!
    </div>
</template>

<script>
export default {
    props: ["delay"],
    data() {
        return {
            showBlock: false
        }
    },
    mounted() {
        setTimeout(() =>{
            this.showBlock = true;
            console.log(this.delay)
        },this.delay)
    },
    updated() {
console.log("component updated")
    },
    unmounted(){

    }
}
</script>

<style>
.block {
    width: 400px;
    border-radius: 20px;
    background: rgb(79, 235, 99);
    color: #fff;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}
</style>