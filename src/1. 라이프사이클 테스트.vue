<template>
  <div>{{ count }}
  </div>
  <h1>Vue.js 라이프사이클 테스트</h1>
</template>

<script>
export default {
  data() {
    return {
      count:0,
    }
  },
  beforeCreate(){
    console.log('LifeCycle is beforeCreate', this.count);
  },
  created(){
    console.log('LifeCycle is created', this.count);
    this.test()
  },
  // beforeMount() {
  //   console.log('LifeCycle is beforeMount', document.querySelector('h1'));
  // },
  // mounted(){
  //   console.log('LifeCycle is mounted', document.querySelector('h1'));
  // },
  methods:{
    test() {
      console.log('함수 호출');
    },
  },
}

// 뷰 기초문법 4
// 1. 선언적 렌더링
// 2. 클래스, 스타일바인딩
// 3. 조건부 렌더링
// 4. 리스트 렌더링
</script>

<style lang="scss" scoped>

</style>

