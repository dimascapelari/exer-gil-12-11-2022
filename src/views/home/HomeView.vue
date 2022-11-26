<template>
  <div class="text-center">
    <h2>Home</h2>
    <edit-user-modal ref="editUserModal" title="Título via props">
    </edit-user-modal>
    <button
      class="btn btn-primary"
      @click="editUserModal.appModal.modal.show()"
    >
      Abrir Modal
    </button>
  </div>
</template>

<script>
import EditUserModal from "./edit-user-modal/edit-user-modal.vue";

export default {
  components: {
    EditUserModal,
  },

  data() {
    return {
      tituloModal: "Home Modal",
      editUserModal: null,
    };
  },
  mounted() {
    this.editUserModal = this.$refs.editUserModal;
    console.log(this.editUserModal);
  },
};
</script>

<style></style>
