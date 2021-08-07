<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <q-card-section class="bg-teal text-white shadow-2">
        <div class="text-h6">Clasificación</div>
      </q-card-section>

      <q-tabs dense active-color="primary" v-model="tab">
        <q-tab label="Pilotos" name="drivers" />
        <q-tab label="Constructores" name="constructors" />
      </q-tabs>

      <q-separator />

      <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="drivers">
          <clasification-table></clasification-table>
        </q-tab-panel>

        <q-tab-panel name="constructors">
          With so much content to display at once, and often so little screen real-estate,
          Cards have fast become the design pattern of choice for many companies, including
          the likes of Google and Twitter.
        </q-tab-panel>
      </q-tab-panels>
    </q-card>
  </div>
</template>

<script>
import { ref } from 'vue';
import clasificationTable from './clasificationTable.vue';

const data = () => ({
  tab: ref('drivers'),
});

export default {
  name: 'Clasification',
  data,
  components: {
    clasificationTable,
  },
};
</script>
