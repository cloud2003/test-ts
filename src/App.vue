<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <List :value="legend"/>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import List from './components/List.vue';
    import {ListAPI} from '@/components/list.api';

    @Component({
        components: {
            List,
        },
    })
    export default class App extends Vue {
        private legend: ListAPI[] = [{
            title: 'Заголовок1',
            color: 'red',
        }, {
            title: 'Заголовок2',
            color: 'blue',
            x: '', // Error
        }];

    }
</script>

<style lang="less">
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
