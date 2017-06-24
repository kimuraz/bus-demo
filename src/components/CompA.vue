<template>
  <div>
    <button v-on:click="emitEvt('Simple')">
      Simple
    </button>
    <button v-on:click="emitEvt('Event')">
      Event
    </button>
    <button v-on:click="emitEvt('Bus')">
      Bus
    </button>
  </div>
</template>

<script>
  import EventBus from '../EventBus';

  export default {
    name: 'compA',
    methods: {
      emitEvt(val) {
        EventBus.$emit('randomEvent', this.evt(val));
      },
      evt: val => val,
    },
  };
</script>
