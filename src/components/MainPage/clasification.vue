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
          <clasification-table :data="drivers"></clasification-table>
        </q-tab-panel>

        <q-tab-panel name="constructors">
          <clasification-table :data="teams"></clasification-table>
        </q-tab-panel>
      </q-tab-panels>
    </q-card>
  </div>
</template>

<script>
import { ref } from 'vue';
import clasificationTable from './clasificationTable.vue';

const drivers = [
  {
    index: 1,
    name: 'L. Hamilton',
    points: 195,
  },
  {
    index: 2,
    name: 'M. Verstappen',
    points: 187,
  },
  {
    index: 3,
    name: 'L. Norris',
    points: 113,
  },
  {
    index: 4,
    name: 'V. Bottas',
    points: 108,
  },
  {
    index: 5,
    name: 'S. Pérez',
    points: 104,
  },
];

const teams = [
  {
    index: 1,
    name: 'Mercedes',
    points: 303,
  },
  {
    index: 2,
    name: 'Red Bull',
    points: 291,
  },
  {
    index: 3,
    name: 'Ferrari',
    points: 163,
  },
  {
    index: 4,
    name: 'McLaren',
    points: 163,
  },
  {
    index: 5,
    name: 'Alpine',
    points: 77,
  },
];

const data = () => ({
  tab: ref('drivers'),
});

export default {
  name: 'Clasification',
  data,
  components: {
    clasificationTable,
  },
  setup() {
    return {
      drivers,
      teams,
    };
  },
};
</script>

<style>
.q-tab-panel {
  padding: 4px 16px;
}
</style>
