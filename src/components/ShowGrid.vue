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
$space:0.2rem;
$size:2.2rem;
.showGrid {
    cursor:pointer;
    background-color:#ccc;
    width:$size;
    height:$size;
    padding:$space;
    border-radius:50%;
    position: fixed;
    right: $space;
    bottom:$space;
    opacity:0.5;
    &.visible {
        background-color:lighten(olivedrab,10);
        opacity:1;
    }
    .showGrid--container {
        background-image:url('../assets/grid.png');
        background-repeat:no-repeat;
        background-size:cover;
        width:$size - $space*2;
        height:$size - $space*2;
        border-radius:50%;
    }
}
</style>


