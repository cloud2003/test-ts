<template>
    <div class="draw-panel legend" v-if="value">
        <div class="group" v-for="item in value">
            <p class="title"><span class="point" :style="{'background-color': item.color}"></span>{{item.title}}</p>
        </div>
    </div>
</template>

<script lang="ts">
    import {Component, Prop, Vue} from 'vue-property-decorator';
    import {ListAPI} from '@/components/list.api';

    @Component({})
    export default class List extends Vue {

        @Prop({default: () => []})
        public value!: ListAPI[];

    }
</script>

<style scoped lang="less">
    .point {
        display: inline-block;
        width: 5px;
        height: 5px;
        border-radius: 50%;
    }
</style>
