<template>
  <div>
    <!-- Button trigger modal -->
    <!-- <button
      type="button"
      class="btn btn-primary"
      data-bs-toggle="modal"
      data-bs-target="#modalDimas"
    >
      Abrir Modal
    </button> -->

    <!-- Modal -->
    <div
      class="modal fade"
      id="modalDimas"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h1 class="modal-title fs-5" id="exampleModalLabel">{{ title }}</h1>
            <button
              type="button"
              class="btn-close"
              aria-label="Close"
              @click="fecharModal"
            ></button>
          </div>
          <div class="modal-body">
            <slot name="modal-body"></slot>
          </div>
          <div class="modal-footer">
            <slot name="modal-footer"></slot>
            <!-- <button
              type="button"
              class="btn btn-secondary"
              @click="fecharModal()"
            >
              Close
            </button> -->
            <button type="button" class="btn btn-primary">Save changes</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "bootstrap/js/dist/modal";

export default {
  data() {
    return {
      modal: null,
    };
  },
  props: {
    title: {
      required: true,
      type: String,
      default: "Preciso de um Título",
    },
  },
  mounted() {
    this.modal = new Modal(document.getElementById("modalDimas"));
    // console.log(this.modal);
  },
  methods: {
    show() {
      this.modal.show();
    },
    fecharModal() {
      this.modal.hide();
    },
  },
};
</script>

<style></style>
