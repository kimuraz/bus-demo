<template>
  <div id="app">
    <comp-a/>
    <comp-b/>
  </div>
</template>

<script>
import CompA from './components/CompA';
import CompB from './components/CompB';

export default {
  name: 'app',
  components: {
    compA: CompA,
    compB: CompB,
  },
};
</script>
