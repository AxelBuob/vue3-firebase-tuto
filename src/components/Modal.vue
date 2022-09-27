<template>
    <div class="backdrop">
        <div class="modal" :class="{sale: theme === 'sale' }">
            <h1>{{ header }}</h1>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: [
            'header',
            'text',
            'theme'
        ],
    }
</script>

<style scoped>
    .backdrop {
        position: fixed;
        top: 0;
        background-color: #000;
        opacity: 0.5;
        width: 100%;
        height: 100%;
    }
    .modal {
        width: 400px;
        padding: 20px;
        margin: 200px auto;
        background: #fff;
        border-radius: 10px;
    }
    .modal > h1 {
        color: green;
    }

    .modal.sale {
        background-color: crimson;
        color: white;
    }

    .modal.sale h1 {
        color: white;
    }
</style>