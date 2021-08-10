<template>
  <span @click="toggleOverlay" class="informational-text">{{ content }}</span>
  <OverlayPanel ref="overlayPanel" :showCloseIcon="true" :dismissable="true" class="p-mr-6 p-ml-6">
    {{ overlayContent }}
  </OverlayPanel>
</template>

<script>
export default {
  name: 'InformationalText',
  props: {
    // Remember basic type checks on props
    content: String,
    overlayContent: String,
  },
  data() {
    return {

    }
  },
  methods:{
    toggleOverlay(event) {
      this.$refs.overlayPanel.toggle(event);
    }
  }
}

</script>


<style scoped>
.informational-text:hover{
  color: #949494;
  cursor: help;
}
.informational-text{
  border-bottom: 1px dashed #999;
  display: inline;
}
.overlay-panel{
  max-width: 50%;
}
</style>


