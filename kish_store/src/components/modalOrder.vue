<template>
    <div class="modal">
        <div class="modal-content">
            <button @click="closeModal">Close</button>
            <img :src="img" alt="">
            <p>{{ name }}</p>
            <p>{{ price }}</p>
        </div>
    </div>
</template>

<script>
export default {
   props: [
    'img',
    'name',
    'price'
   ],
   methods: {
    closeModal() {
        this.$emit('close')
    }
   }
}
</script>
<style>
    .modal {
        position: absolute;
        z-index: 100;
    }
</style>