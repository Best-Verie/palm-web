<template>
    <div>
        <h2>Header</h2>
        <h3>{{message}}</h3>
        <h4>Working from {{location}}</h4>
    </div>
</template>

<script lang="ts">
import vue from 'vue'

export default vue.extend({
    data() {
        return {
            message: 'We are PayingTon',
            location: 'Rwanda',            
        }
    },

    computed: {
        location (): string {
            return `${this.location}`
        }
    }
})
</script>

<style scoped>

</style>