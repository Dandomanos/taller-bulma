<template>
    <div @click="update" class="showGrid" :class="{'visible':show}">
        <div class="showGrid--container">
            <!-- <img src="../../static/eye.svg" alt=""> -->
        </div>
    </div>
</template>

<script>
export default {
    props:['show'],
    methods: {
        update() {
            this.$emit('update', !this.show)
        }
    }
}
</script>
<style lang="scss"> 
.showGrid {
    cursor:pointer;
    background-color:#ccc;
    width:2.2rem;
    height:2.2rem;
    padding:0.2rem;
    border-radius:50%;
    position: fixed;
    right: 1rem;
    bottom:1rem;
    opacity:0.5;
    &.visible {
        background-color:lighten(olivedrab,10);
        opacity:1;
    }
    .showGrid--container {
        background-image:url('../assets/grid.png');
        background-repeat:no-repeat;
        background-size:cover;
        width:1.8rem;
        height:1.8rem;
        border-radius:50%;
    }
}
</style>


