<template>
    <button @click="onClick()" :style="{ background: color }" class="btn">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: {
            type: String,
            required: true
        },
        color: {
            type: String,
            required: true
        }
    },
    methods: {
        onClick() {
            console.log('click');
            this.$emit('click')
        }
    }
}
</script>
