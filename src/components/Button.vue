<template>
    <button 
        class="btn" 
        :style="{ background: color }"
        @click="onClick()"
    >
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: {
            type: String
        },
        color: {
            type: String
        }
    },
    methods:{
        onClick() {
            this.$emit('btn-click');
        }
    }
}
</script>