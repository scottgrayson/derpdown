<template>
    <div class="derpdown">
        <div @click="toggle">
            <slot name="toggle"></slot>
        </div>
        <div class="derpdown-content" v-show="show"
            :class="{ 'derpdown-right' : align_right }">
            <slot name="content"></slot>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                show: false
            }
        },
        props: {
            align_right: {
                type: Boolean,
                default: false
            },
        },
        methods: {
            toggle() {
                this.show = !this.show
            },
        }
    }
</script>

<style>
.derpdown-content {
    position: absolute;
}
.derpdown {
    position: relative;
}
.derpdown-right {
    right: 0;
}
</style>
