<template>
  <q-layout view="hHh lpR ffr">

    <q-header elevated class="q-pa-md bg-primary text-white">
      <q-toolbar class="centered-nav">
        <q-toolbar-title class="flexed-nav">
          <div class="flexed-title">
            <p class="hepta web-name">Impeccable Ninja</p>
          <div class="hepta text-h3 my-name">
            by Otabek-Sadiridinov
          </div>
          </div>
          <div class="q-ml-lg">
            <div class="q-focus-helper">
              <q-btn flat label="YouTube" @click="clickHandler1"/>
            </div>
            <q-btn flat label="Courses" @click="clickHandler2"/>
            <q-btn flat label="Resources" @click="clickHandler3"/>
        </div>
        </q-toolbar-title>
          <div>
                    <q-btn dense flat round icon="fab fa-youtube" to />
        <q-btn dense flat round icon="fab fa-facebook-f" to />
        <q-btn dense flat round icon="fab fa-instagram" to />
        <q-btn dense flat round icon="fab fa-telegram-plane" to />
          </div>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="right" side="right" bordered content-class="bg-primary">
      <q-list>
        <q-item-label header>Essential Links</q-item-label>
        <q-item clickable tag="a" target="_blank" href="https://quasar.dev">
          <q-item-section avatar>
            <q-icon name="school" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Docs</q-item-label>
            <q-item-label caption>quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://github.quasar.dev">
          <q-item-section avatar>
            <q-icon name="code" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Github</q-item-label>
            <q-item-label caption>github.com/quasarframework</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://chat.quasar.dev">
          <q-item-section avatar>
            <q-icon name="chat" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Discord Chat Channel</q-item-label>
            <q-item-label caption>chat.quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://forum.quasar.dev">
          <q-item-section avatar>
            <q-icon name="record_voice_over" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Forum</q-item-label>
            <q-item-label caption>forum.quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://twitter.quasar.dev">
          <q-item-section avatar>
            <q-icon name="rss_feed" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Twitter</q-item-label>
            <q-item-label caption>@quasarframework</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://facebook.quasar.dev">
          <q-item-section avatar>
            <q-icon name="public" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Facebook</q-item-label>
            <q-item-label caption>@QuasarFramework</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container class="bg-primary">
      <router-view />
    </q-page-container>

    <q-footer bordered class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">
          </q-avatar>
          Title
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
export default {
  name: 'MyLayout',
  data () {
    return {
      right: false
    }
  }
}
</script>

<style>
.flexed-nav {
  display: -webkit-flex;
  display: -moz-flex;
  display: -ms-flex;
  display: -o-flex;
  display: flex;
  -ms-align-items: center;
  align-items: center;
  margin-left: 12px;
}
.centered-nav {
  width: 100%;  
  display: -webkit-flex;
  display: -moz-flex;
  display: -ms-flex;
  display: -o-flex;
  display: flex;  
  -ms-align-items: center;
  align-items: center;  
  justify-content: space-around;
}
.flexed-title {
  display: block;
  -ms-align-items: center;
  align-items: center;
  justify-content: flex-start;
}
p {
    display: block;
    margin-block-start: 0em;
    margin-block-end: 0em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
}
.web-name {
  font-weight: bold;
  font-size: 30px;
  margin: 0;
}
.my-name {
  display: block;
  font-size: 100%;
  line-height: 1;
}
@media screen and (max-width: 860px) {
  .my-name {
    display: none;
  }
}
</style>