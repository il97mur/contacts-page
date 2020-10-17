<template>
    <section class="feedback bg-light">
        <form action="" method="post" id="ajax_form" class="feedback-form">
            <h2 class="h2">Форма обратной связи</h2>
            <div class="form-group">
            <label for="exampleInputEmail1">Ваше имя</label>
            <input type="text" name="name" class="form-control" id="exampleInputEmail1">
            </div>
            <div class="form-group">
                <label for="exampleInputPassword1">Ваш телефон</label>
                <input type="tel" name="phonenumber" class="form-control" id="exampleInputPassword1">
            </div>
            <div class="form-group form-check">
                <input type="checkbox" class="form-check-input" id="exampleCheck1">
                <label class="form-check-label" for="exampleCheck1">Check me out</label>
            </div>
            <button type="button" class="btn btn-primary submit-button">Submit</button>
        </form>
        <div id="result_form"></div> 
    </section>

</template>

<script>
export default {
    mounted() {

            function sendAjaxForm(result_form, ajax_form, url) {
        $.ajax({
            url:     url, //url страницы (action_ajax_form.php)
            type:     "POST", //метод отправки
            dataType: "html", //формат данных
            data: $("#"+ajax_form).serialize(),  // Сеарилизуем объект
            success: function(response) { //Данные отправлены успешно
                result = $.parseJSON(response);
                $('#result_form').html('Имя: '+result.name+'<br>Телефон: '+result.phonenumber);
            },
            error: function(response) { // Данные не отправлены
                $('#result_form').html('Ошибка. Данные не отправлены.');
            }
        });
    }

        $( document ).ready(function() {
        $(".submit-button").click(
            function(){
                sendAjaxForm('result_form', 'ajax_form', 'static/php/action_ajax_form.php');
                return false; 
            }
        );
    });
    

        }
}


</script>

<style>
    .h2 {
        margin-bottom: 30px;
    }
    .feedback {
        width: 70%;
        border: 1px solid #ccc;
        border-radius: 20px;
        padding: 20px 30px;
        margin: 0px auto 0px auto;  
    }
</style>