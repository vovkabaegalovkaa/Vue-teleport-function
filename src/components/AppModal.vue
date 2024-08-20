<template>
    <div class="modal-back" @click="$emit('closeModal')"></div>
    <div class="modal">
        <h3>Заголовок модального окна</h3>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Exercitationem, commodi! Quia aliquid asperiores nobis ex eius repellendus eligendi quasi et?</p>
    </div>
</template>

<script>
export default {
    emits: ['closeModal']
}
</script>