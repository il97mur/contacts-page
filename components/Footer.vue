<template>
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="col-6 col-md-4 d-flex align-items-center footer__logo">
                    CORNLAB
                </div>
                <div class="col-3">
                    <div class="col-12 d-flex flex-column">
                        <p class="text footer__heading">Навигация</p>
                        <nuxt-link class="footer__link" to="/">Homepage</nuxt-link>
                        <nuxt-link class="footer__link" to="/about">About Us</nuxt-link>
                        <nuxt-link class="footer__link" to="/contacts">Contacts</nuxt-link>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style>
    .footer {
        display: flex;
        justify-content: center;
        background-color: #222;
        width: 100%;
        padding: 100px 0px;
    }
    .footer__logo {
        font-size: 40px;
        color: #fff;
    }
    .footer__heading {
        color: #fff;
        font-weight: bold;
        font-size: 20px;
    }
    .footer__link {
        text-decoration: none;
        color: #cccccc;
    }
    .footer__link:hover {
        color: #eee
    }
</style>