<template>
    <div>
        <!-- <div v-if="isVisible" class="red"></div>
        <div v-if="isVisible == true" class="blue"></div>
        <div v-else="false" class="black"></div> -->

        <!-- <div v-if="count > 1" class="red"></div>
        <div v-else class="blue"></div>
        <button @click="count--">◀</button>
        <button @click="count++">▶</button> -->

        <div v-show="isVisible" class="red"></div>
        <div v-show="!isVisible" class="blue"></div>
        <div v-if="isVisible" class="black"></div>
        <!-- v-if : DOM에 남지 않는다
        v-show : DOM에 남아있다. -->

    </div>
</template>

<script>
export default {
    data () {
        return {
            isVisible: false,
            count: 0,
        }
    }
}
</script>

<style scoped>
.red {
    width: 100px;
    height: 100px;
    background-color: red;
}
.blue {
    width: 100px;
    height: 100px;
    background-color: blue;
}
.black {
    width: 100px;
    height: 100px;
    background-color: black;
}

</style>