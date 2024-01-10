<script setup>
import { ref } from 'vue';

const email = ref("Trang");
const handleLogEmail = () => {
    console.log(email.value);
}
</script>

<template>
    <div>
        <form action="">
            <input type="text" v-model="email">
            <button @click.prevent="handleLogEmail">Summit</button>
        </form>
    </div>
</template>



<style lang="scss" scoped></style>