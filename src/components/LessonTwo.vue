<script setup>
import { computed, reactive, ref } from 'vue';

const authours = reactive({
    authour: "Nguyễn Thị Trang",
    books: [
        "Vue 1",
        "Vue 2",
        "Vue 3"
    ]
})

const handleMessage = computed(() => {
    return authours.books.length > 0 ? "Yes" : "No";
})

const handleMessage2 = computed({
    get() {
        return authours.books.length > 0 ? "Yes" : "No";
    },
    set(newValue) {
        authours.authour = newValue
    }
})
const isActive = ref(true);
const classObj = {
    active: isActive,
    error: !isActive
}
const xoa = () => {
}
</script>

<template>
    <div>
        <p>{{ handleMessage }}</p>
        <h1 :class="classObj">Hello</h1>
        <button @click="xoa()">jkdsajl</button>
    </div>
</template>



<style lang="css" scoped>
.active {
    color: green;
}

.error {
    color: red;
}
</style>