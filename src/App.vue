<template web>
  <div class="w-page">
    <div class="w-container">
      <img src="~/assets/logo.png" alt="logo" height="20%" width="20%" />
      <HelloWorld :msg="msg" />
    </div>
  </div>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle" />
    <GridLayout rows="auto, auto">
      <HelloWorld :msg="msg" />
    </GridLayout>
  </Page>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "~/components/HelloWorld.vue";

const { VUE_APP_MODE, VUE_APP_PLATFORM } = process.env;

@Component({
  name: "home",
  components: {
    HelloWorld
  }
})
export default class App extends Vue {
  private navbarTitle = `App.vue`;
  private msg = `Mode=${VUE_APP_MODE} and Platform=${VUE_APP_PLATFORM}`;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
