<script setup>
    import Question from "../components/Question.vue"
    import Header from "../components/QuizHeader.vue"
    import {useRoute} from "vue-router"
    import { ref } from "vue"
    import quizes from "../data/quizes.json"


    const route = useRoute()
    const quizId = parseInt(route.params.id)

    const quiz = quizes.find(q => q.id === quizId)

    const currentQuestionIndex = ref(0)

    const questionStatus = `${currentQuestionIndex}/${quiz.questions.length}`

</script>


<template>
    <div>
        <Header :questionStatus="questionStatus"/>
        <div>
            <Question :question="quiz.questions[currentQuestionIndex]"/>
        </div>
    </div>
</template>

<style scoped>
    
</style>