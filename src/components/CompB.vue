<template>
  <p>{{ eventValue }}</p>
</template>

<script>
  import EventBus from '../EventBus';

  export default {
    name: 'compB',
    data() {
      return {
        eventValue: '',
      };
    },
    created() {
      EventBus.$on('randomEvent', this.sendToData);
    },
    methods: {
      sendToData(val) {
        if (val) {
          this.$data.eventValue = val;
        }
      },
    },
  };
</script>
