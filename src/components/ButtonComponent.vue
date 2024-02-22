<template>
    <button
    type="button"
    :style="buttonStyles"
    :class="['customBtn']"
    @click="handleClick"
    :disabled="disabled"
    >
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'ButtonComponent',
    props: {
        buttonStyles: {
            type: Object,
            default: () => ({}),
        },
        disabled: {
            type: Boolean,
            default: false,
        },
    },
    methods: {
        handleClick() {
            this.$emit('click');
        },
    }
}
</script>

<style scoped>
    .customBtn {
        background-color: rgba(79, 98, 246, 1);
        border-radius: 60px;
        padding: 20px 64px;
        color: rgba(255, 255, 255, 1);
        font-size: 16px;
        line-height: 14px;
        letter-spacing: 0.164px;
        text-align: center;
        border: 0;
    }

    .customBtn:hover {
        background-color: rgba(113, 129, 252, 1);
    }

    .customBtn:disabled {
        background-color: rgba(224, 224, 224, 1);
        color: rgba(130, 130, 130, 1);
        cursor: not-allowed;
    }

    .customBtn:active {
        background-color: rgba(53, 75, 244, 1);
    }
</style>