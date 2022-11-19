<template>
  <app-modal ref="appModal"> </app-modal>
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
