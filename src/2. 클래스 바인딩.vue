<template>
    <div>{{ rawHtml }}</div>   
    <div>{{ rawHtml2 }}</div>
    <h1 v-html="rawHtml2"></h1>

    <h2 v-bind:class="{ active:isActive }">클래스 바인딩 테스트</h2>
    <h2 :class="{ active:isActive}">클래스 바인딩 테스트</h2>
    <button @click="change">버튼</button>

    <h3 style="color: green; font-size: 20px">스타일 바인딩 테스트</h3>
    <h3 :style="{color:fontColor, fontSize: fontSize + 'px'}">스타일 바인딩 테스트</h3>
</template>
<script>
export default {
    data() {
        return {
            rawHtml: '텍스트 출력',
            rawHtml2: '<span style="color:red"">텍스트 출력2</span>',
            isActive: false,
            fontColor: 'yellow',
            fontSize: 20,
        }
    },
    methods: {
        change() {
            this.isActive = !this.isActive
        },
    },
}
</script>
<style scoped>
h2.active {
    color : blue;
}
</style>