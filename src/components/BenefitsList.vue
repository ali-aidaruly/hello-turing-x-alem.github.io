<template>
    <div class="benefits">
        <div v-for="item in benefits" :key="item" class="benefits__item">
                {{ item }}
        </div>
    </div>
</template>

<script>
export default {
    setup() {
        const benefits = [
            '🇰🇿 We will strive to give you the real insights on KZ market and beyond',
            '🎯 We will strive to provide you with the most productive environment in your life',
            '🔥 We will strive to help you become coding gurus && software engineering jedis',
            '📣 We will strive to make a proactive and versatile person with a diversity of soft skills'
        ]
        return {
            benefits
        }
    }
}
</script>

<style lang="scss">
.benefits {
    &__item {
        font-size: 18.72px;
        font-weight: 400;
        padding: 20px;
        margin-bottom: 10px;
        border-radius: 5px;
        background-color: rgba(0,0,0,.05);
    }
}
</style>
