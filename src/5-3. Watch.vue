
<template>
    <button @click="isChange">{{ message }}</button>
    <label>{{ watchMessage }}</label>


    
</template>

<script>
export default {
    data () {
        return {
            message:"Watch 기능 테스트 오리지널.",
            watchMessage:'',
        }
    },
    watch: {
        message() {
            window.alert('message 변수 데이터 변경됨');
            this.watchMessage = 'Watch 동작';
        }
    },
    methods: {
        isChange(){
            console.log('함수 호출');
            this.message = '변경된 message 데이터'
            
        }
    }
}

</script>

<style lang="scss" scoped>

</style>
 
