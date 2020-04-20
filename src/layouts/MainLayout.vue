<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-grey-1">
      <q-toolbar class="q-py-lg q-px-xl">
        <q-btn flat label="Music" color="primary"/>
        <q-btn flat label="Podcast" color="black" />
        <q-btn flat label="Live" color="black"/>
        <q-space />
        <q-input dense color="lime-11" outlined placeholder="Type here to search">
          <template v-slot:prepend>
            <q-icon name="search" />
          </template>
        </q-input>
        <q-space />
        <q-btn flat round dense icon="notifications" color="black" class="q-mr-md" size="sm">
          <div style="border-radius: 50%; width: 10px; height: 10px;" class="q-badge--floating bg-primary"></div>
        </q-btn>
        <q-btn flat round dense icon="settings" color="black" class="q-mr-lg" size="sm" />
        <div class="flex bg-grey-9 rounded-borders items-center">
          <div class="bg-grey-8 q-pa-sm rounded-borders">
            <q-avatar rounded size="sm">
              <img src="/statics/avatar.jpeg">
            </q-avatar>
          </div>
          <div class="text-white q-pa-sm text-bold text-caption">
            Vinicius Berger
          </div>
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer
      show-if-above
      content-class="bg-grey-3"
    >
      <div class="text-h6 q-px-xl q-py-lg">
        Groovvy
      </div>
      <q-list class="q-py-lg">
        <q-item-label
          header
          class="text-grey-8 q-px-xl text-uppercase"
        >
          Menu
        </q-item-label>

        <q-item clickable v-ripple class="q-px-xl">
          <q-item-section avatar>
            <q-icon color="primary" name="bluetooth" size="xs" />
          </q-item-section>
          <q-item-section>Explore</q-item-section>
        </q-item>

        <q-item clickable v-ripple class="q-px-xl">
          <q-item-section avatar>
            <q-icon color="primary" name="build" size="xs" />
          </q-item-section>
          <q-item-section>Genres</q-item-section>
        </q-item>
      </q-list>
      <q-list class="q-pt-lg">
        <q-item-label
          header
          class="text-grey-8 q-px-xl text-uppercase"
        >
          Library
        </q-item-label>

        <q-item clickable v-ripple class="q-px-xl">
          <q-item-section avatar>
            <q-icon color="primary" name="bluetooth" size="xs" />
          </q-item-section>
          <q-item-section>Explore</q-item-section>
        </q-item>

        <q-item clickable v-ripple class="q-px-xl">
          <q-item-section avatar>
            <q-icon color="primary" name="build" size="xs" />
          </q-item-section>
          <q-item-section>Genres</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',

  data () {
    return {
    }
  }
}
</script>
