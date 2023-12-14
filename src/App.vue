<template>
    <h1>{{ count }}</h1>
</template>

<script>
export default {
    data() {
        return {
            count: 2
        }
    },
    //작성하는 순서는 중요하지 않음. created가 먼저 실행되고 mounted가 실행됨.
    beforeCreate() {
        console.log('Before Create!', this.count)
    },
    created() {
        console.log('Created!', this.count)
        console.log(document.querySelector('h1'))
    },
    beforeMount() {
        console.log('Before Mount!')
        console.log(document.querySelector('h1'))
    },
    mounted() {
        console.log('Mounted!')
        console.log(document.querySelector('h1'))
    }
}
</script>