
<template>
  <div>
    <Add @result="handleResult" />
    <Subtract @result="handleResult" />
    <Divide @result="handleResult" />
    
    <div>Result: {{ result }}</div>
  </div>
</template>

<script>
import Add from './Add.vue';
import Subtract from './Subtract.vue';
import Divide from './Divide.vue';


export default {
  components: { Add, Subtract, Divide },
  data() {
    return {
      result: null,
    };
  },
  methods: {
    handleResult(value) {
      this.result = value;
    },
  },
};
</script>
