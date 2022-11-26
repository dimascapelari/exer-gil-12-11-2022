<template>
  <app-modal ref="appModal">
    <template v-slot:modal-body>
      <h4>Conteúdo via slot</h4>
    </template>
    <template v-slot:modal-footer>
      Botão via Slot
      <button
        type="button"
        class="btn btn-danger"
        @click="appModal.fecharModal"
      >
        Close
      </button>
    </template>
  </app-modal>
</template>

<script>
import AppModal from "@/components/app-modal/app-modal.vue";

export default {
  components: {
    AppModal,
  },
  data() {
    return {
      appModal: null,
    };
  },
  mounted() {
    this.appModal = this.$refs.appModal;
  },
};
</script>

<style></style>
