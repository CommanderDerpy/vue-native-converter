<template web>
  <div class="w-page">
    <div class="w-container">
      <span>This is an about page</span>
    </div>
  </div>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle" />
    <GridLayout>
      <Label
        text="This is an about page"
        textWrap="true"
        horizontalAlignment="center"
        verticalAlignment="center"
      />
    </GridLayout>
  </Page>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  name: "about"
})
export default class About extends Vue {
  private navbarTitle = `About.vue`;
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
