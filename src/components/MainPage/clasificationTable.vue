<template>
    <q-table
      :rows="data"
      :columns="columns"
      row-key="index"
      flat
      :rows-per-page-options="[0]"
      hide-header
      hide-bottom
    />
</template>

<script>

const props = {
  data: {
    type: Array,
    default: () => [],
  },
};
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

export default {
  name: 'ClasificationTable',
  setup() {
    return {
      columns,
    };
  },
  props,
};
</script>
