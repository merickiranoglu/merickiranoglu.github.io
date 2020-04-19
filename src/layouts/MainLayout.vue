<template>
  <q-layout view="hHh lpR lFf">

    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title>
        <div class="col" style="align-items: center; display: flex; justify-content: center; letter-spacing: 0.25em;" >Meriç Kıranoğlu</div>
        </q-toolbar-title>
      </q-toolbar>

    </q-header>

    <q-drawer show-if-above v-model="left" side="left" bordered>
    <div class="col q-my-xl" style="align-items: center; display: flex; justify-content: center;">
     <q-img id= "imgProfilePicture"
        :src="'/statics/images/IMG_6249-min.JPG'"
      />
    </div>
    <div class="col" style="align-items: center; display: flex; justify-content: center;">
     <q-list>
        <q-item to="/" clickable>
          <q-item-section avatar>
            <q-icon name="person_pin"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>About Me</q-item-label>
          </q-item-section>
        </q-item>

        <q-item to="/education" clickable>
          <q-item-section avatar>
            <q-icon name="school"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Education</q-item-label>
          </q-item-section>
        </q-item>

        <q-item to="/experience" clickable>
          <q-item-section avatar>
            <q-icon name="work"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Experience</q-item-label>
          </q-item-section>
        </q-item>

        <q-item to="/skills" clickable>
          <q-item-section avatar>
            <q-icon name="share"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Skills</q-item-label>
          </q-item-section>
        </q-item>

        <q-item to="/repositories" clickable>
          <q-item-section avatar>
            <q-icon name="developer_mode"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Repositories</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </div>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      left: false
    }
  }
}
</script>
