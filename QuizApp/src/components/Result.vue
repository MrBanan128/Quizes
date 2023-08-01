<script setup>
    import { RouterLink } from 'vue-router';
    const {quizQuestionLength,CorrectNumber} = defineProps(["quizQuestionLength","CorrectNumber"])
</script>

<template>
    <div class="result">
        <p>Your Results...</p>
        <h1>{{ CorrectNumber }} / {{ quizQuestionLength }}</h1>
        <RouterLink to="/">Go Back</RouterLink>
    </div>
</template>

<style scoped>
    .result {
        text-align: center;
        padding: 100px 0;
    }
    p{
        font-size: 25px;
    }
    h1{
        font-size: 40px;
    }
</style>