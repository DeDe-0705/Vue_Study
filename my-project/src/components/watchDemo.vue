<template>
    <div>
        <input v-model="name" />
        <input v-model="info.city" />
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: "dede",
            info: {
                city: "海南"
            }
        }
    },
    watch: {
        name(newVal, oldVal) {
            console.log("watch name", newVal, oldVal);
        },
        info: {
            handle(oldVal, val) {
                console.log("watch info", newVal, oldVal);
            }
        },
        deep: true
    }
}
</script>