<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="main-toolbar">
          <div class="row items-center cursor-pointer non-selectable">
            <div class="q-mx-md">
            Clasificación
            <q-menu>
              <q-list style="min-width: 100px">
                <q-item clickable v-close-popup>
                  <q-item-section>Pilotos</q-item-section>
                </q-item>
                <q-item clickable v-close-popup>
                  <q-item-section>Constructores</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
            </div>
          </div>
          <div class="row items-center cursor-pointer">
            <div class="q-mx-md">
            Circuitos
            </div>
          </div>
          <div class="row items-center cursor-pointer">
            <div class="q-mx-md">
            Pilotos
            </div>
          </div>
          <div class="row items-center cursor-pointer">
            <div class="q-mx-md">
            Equipos
            </div>
          </div>
          <div class="row items-center cursor-pointer">
            <div class="q-mx-md">
            Histórico
            </div>
          </div>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
};
</script>

<style lang="scss">
.main-toolbar {
  background-color: $primary;
  font-size: 18px;
  padding: 0;
.cursor-pointer {
  min-height: inherit;
  &:hover {
    background-color: $primary-hover;
  }
}
}

</style>
