<template>
    <Page class="page">
        <ActionBar class="action-bar">
            <Label class="label" text="Home"/>
        </ActionBar>

        <GridLayout columns="*" rows="*">
          <Label class="label" col="1" row="1" v-bind:text="message"/>
        </GridLayout>
    </Page>
</template>

<script>
  export default {
    computed: {
      message() {
        return "Welcome!";
      }
    }
  };
</script>

<style scoped lang="scss">
    @import '~@nativescript/theme/scss/variables/blue';

    // Custom styles
    .fas {
        @include colorize($color: accent);
    }
</style>
