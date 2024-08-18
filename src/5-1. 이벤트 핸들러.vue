
 <template>
    <div id="event1">
       <button @click="count++">인라인 핸들러</button>
        <span> {{ count }}</span>
        <br><br>
        <button @click="isChange">메서드 핸들러</button>
        <span> {{ name }}</span>
    </div>


    
</template>

<script>
export default {
    data () {
        return {
         count:0,
         name:'Vue.js',
        }
    },
    methods: {
        isChange() {
            this.name = '변경'
        }

    }

}

</script>

<style lang="scss" scoped>

</style>
 
