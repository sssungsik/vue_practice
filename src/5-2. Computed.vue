
<template>
    <div id="event1">
      <h1>{{text}}</h1>
      <h1>함수 호출 값 : {{ isChange() }}</h1>
      <h1>함수 호출 값 : {{ isChange() }}</h1>
      <h1>함수 호출 값 : {{ isChange() }}</h1>
      
      <h2> {{ isComputed }}</h2>
      <h2> {{ isComputed }}</h2>
      <h2> {{ isComputed }}</h2>
    </div>


    
</template>

<script>
export default {
    data () {
        return {
        text:'Computed 테스트 데이터.',
        }
    },
    computed: {
        isComputed() {
            console.log('computed 기능 생성');
            
            return this.text.split("").reverse().join('')
        }
    },
    methods: {
        isChange() {
            console.log('함수 호출')
            console.log(this.text)
            return this.text.split("").reverse().join('')
            
            
        }
    }
}

</script>

<style lang="scss" scoped>

</style>
 
