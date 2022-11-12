<template>
  <div class="text-center">
    <h2>Home</h2>
    <CompModal :title="tituloModal" ref="dimasModal">
      <template v-slot:modal-body>
        <h3>Conteúdo do Modal via slot</h3>
      </template>
      <template v-slot:modal-footer>
        <button class="btn btn-dark" @click="fecharModal">Fechar</button>
      </template>
    </CompModal>
    <button class="btn btn-primary" @click="abrirModal">Abrir Modal</button>
  </div>
</template>

<script>
import CompModal from "../components/CompModal.vue";

export default {
  components: {
    CompModal,
  },

  data() {
    return {
      tituloModal: "Home Modal",
      dimasModal: null,
    };
  },
  mounted() {
    this.dimasModal = this.$refs.dimasModal;
  },
  methods: {
    abrirModal() {
      this.dimasModal.show();
    },
    fecharModal() {
      this.dimasModal.fecharModal();
    },
  },
};
</script>

<style></style>
