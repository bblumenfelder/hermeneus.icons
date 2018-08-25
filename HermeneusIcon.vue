<template>
    <div>
        <img :src="icon" :width="CalcWidth" :height="CalcHeight" alt="">
    </div>
</template>

<script>
    let IconPathString = {
        'success': '/img/svg/iris-icon-success.svg',
        'danger': '/img/svg/iris-icon-danger.svg',
        'info': '/img/svg/iris-icon-info.svg',
        'warning': '/img/svg/iris-icon-danger.svg',
        'confirm': '/img/svg/iris-icon-confirm.svg',
    };

    export default {
        name: "hermeneus-icon",
        props: ['name', 'width', 'height'],
        computed: {
            CalcWidth: function () {
                return this.width ? this.width : '15';
            },
            CalcHeight: function () {
                return this.height ? this.height : '15';
            },
            icon: function () {
                return IconPathString[this.name]
            }
        }
    }
</script>

<style scoped>

</style>