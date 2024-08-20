<template>
  <div class="container">
    <h2>Teleports</h2>
    <button class="btn" @click="modalStatus = true">Открыть модальное окно</button>
    <teleport to="body">
      <app-modal v-if="modalStatus" @closeModal="modalStatus = false"></app-modal>
    </teleport>
    <!-- Теперь наше модальное окно врезается в DOM и хоть оно и выглядит нормально, все равно структура сайта рушится, с этим и 
    помогут телепорты
    Телепорт – это тег, которого нет в HTML, а добавляет его сюда именно Vue. 
    У тега есть два аттрибута: to – отвечает за то, в какую область DOM будет перенесено содержимое тега(указывается через css-селектор)
    Аттирбут disabled для котрого не нужны значения, он просто отменяет телепортацию, ну мало ли что-->
  </div>
</template>

<script>
import AppModal from './components/AppModal.vue';
export default {
  data(){
    return {
      modalStatus: false,
    }
  },
  components: {
    'app-modal': AppModal,
  }
}
</script>


