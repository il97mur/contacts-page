

<template>
    <section class="contacts">
        <div class="container contacts__container">
            <h1 class="w-100 h1 contacts__h1">Контакты</h1>

            <div class="row">
                <div class="col-6">
                    <p class="contacts__contact">Наш телефон: +7900000000</p>
                    <p class="contacts__contact">Емайл: example@mail.ru</p>
                    <p class="contacts__contact">Адрес: Россия, Красная Площадь</p>
                </div>
                <div class="col-6">

                </div>
            </div>


        </div>
        <FeedbackForm />

    </section>
</template>

<script>
import FeedbackForm from '@/components/FeedbackForm.vue'

export default {
    components: {
        FeedbackForm
    }
}
</script>

<style>
    .contacts {}
    .contacts__container {
        margin-bottom: 40px;
    }
    .contacts__contact {
        margin-bottom: 10px;
    }
    .contacts__h1 {
        margin-bottom: 30px;
    }
</style>