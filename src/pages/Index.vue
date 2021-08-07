<template>
  <q-page>
    <div class="row q-pa-md">
      <div class="col-4">
        <clasification></clasification>
      </div>
      <div class="col-6"></div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import clasification from '../components/MainPage/clasification.vue';

export default defineComponent({
  name: 'PageIndex',
  components: {
    clasification,
  },
});
</script>
