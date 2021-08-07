<template>
    <q-table
      :rows="rows"
      :columns="columns"
      row-key="index"
      virtual-scroll
      :rows-per-page-options="[0]"
      hide-header
      hide-bottom
    />
</template>

<script>
const columns = [
  {
    name: 'index',
    label: 'POS.',
    field: 'index',
  },
  {
    name: 'name',
    required: true,
    label: 'Piloto',
    align: 'left',
    field: (row) => row.name,
    format: (val) => `${val}`,
    sortable: true,
  },
  {
    name: 'points', align: 'center', label: 'Pts.', field: 'points', sortable: true,
  },
];

const rows = [
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

export default {
  name: 'ClasificationTable',
  setup() {
    return {
      columns,
      rows,
    };
  },
};
</script>
