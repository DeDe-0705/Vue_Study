<template>
    <div>
        <p :class="{ black: isBlack, yellow: isYellow }">使用class</p>
        <p :class="[black, yellow]">使用 class (数组) </p>
        <p :style="styleData">使用 style</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isBlack: true,
            isYellow: true,

            black: 'black',
            yellow: 'yellow',

            styleData: {
                fontSize: '40px',
                color: 'red',
                backgroundColor: '#ccc'
            }
        }
    }
}
</script>