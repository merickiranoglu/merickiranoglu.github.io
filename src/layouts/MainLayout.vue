<template>
  <q-layout view="hHh lpR lFf">

    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />
        <q-toolbar-title>
            <div style="font-size: 16px; display: flex; justify-content: center;">
            <span style="align-items: center; letter-spacing: 0.25em;">
            Meriç Kıranoğlu
            </span>
            <span class="q-pl-xl">
            <a href="https://www.linkedin.com/in/mkiranoglu/">
              <i class="fab fa-linkedin-in fa-md" style="color: white;"></i>
            </a>
            </span>
            <span class="q-pl-md">
            <a href="https://github.com/merickiranoglu">
              <i class="fab fa-github fa-md" style="color: white;"></i>
            </a>
            </span>
          </div>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="left" side="left" bordered>
    <div class="col q-ma-xl" style="align-items: center; display: flex; justify-content: center; width: 200px; height: 300px">
     <q-img id= "imgProfilePicture"
        :src="'/statics/images/IMG_6249-min.jpg'"
      />
    </div>
    <div class="col" style="align-items: center; display: flex; justify-content: center; padding: 8px 32px 8px 16px;">
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
