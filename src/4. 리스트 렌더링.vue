<!-- 
 리스트 렌더링
 - 배열 데이터를 기반으로 동일한 구조의 UI 반복 호출
 - v-for 디렉티브 사용 
 -->
<template>
    <!-- 기존 html 코드 -->
    <div style="color: blue;">
        <li>{{ sampleArray[0] }}</li>
        <li>{{ sampleArray[1] }}</li>
        <li>{{ sampleArray[2] }}</li>
        <li>{{ sampleArray[3] }}</li>
    </div>

    <!-- v-for 디렉티브 사용 -->
    <div style="color: red">
        <li v-for="(item, index) in sampleArray" :key="item" @click="openDialog(index)">{{ item }} / {{ index }}</li>
        <li v-for="(user, i) in users" :key="user.name">{{ user.도 }} / {{ user.시 }} / {{ i + 1 }}</li>
    </div>


    
</template>

<script>
export default {
    data () {
        return {
            sampleArray: ['가','나', '다','라'],
            users:[
                { 도 : '전북', 시:'전주'},
                { 도 : '인천', 시:'부평'},
                { 도 : '경기', 시:'파주'},
                { 도 : '전북', 시:'순창'},
            ]
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
 
