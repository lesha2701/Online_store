<template>
    <div class="modal__inner">
        <div class="model__title">
            <h2>Корзина</h2>
        </div>
        <div v-for="todo in todos" :key="todo.id" class="modal">
            <img class="modal__item-img" :src="todo.img" alt="">
            <div class="modal__item-text">
                <p>{{ todo.name }}</p>
                <p>{{ todo.price}}</p>
            </div>
            <a class="modal__delete" href="#">Удалить</a>
        </div>
        <a class="order" href="">Заказать</a>
    </div>
</template>
<script>
export default {
    props: {
        todos: {
            type: Array,
            required: true,
        }
        
    },
}
</script>
<style>
    .modal__inner {
        display: flex;
        flex-direction: column;
        margin-top: 20px;
        border: 1px solid #F8B101;
        padding: 10px 20px;
    }

    .model__title {
        text-align: center;
    }

    .modal {
        margin-top: 10px;
        display: flex;
        align-items: center;
        gap: 20px;
        position: relative;
    }

    .modal__delete {
        margin-left: auto;
    }

    .modal__item-img {
        width: 100px;
        align-self: center;
    }

    .order {
        margin-top: 10px;
        margin: 10px auto;
        width: 140px;
        padding: 7px 20px;
        background-color: #F8B101;
        color: #000000;
        font-weight: 400;
        font-size: 24px;
        line-height: 150%;
        text-decoration: none;
    }
</style>