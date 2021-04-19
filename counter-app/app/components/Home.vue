<template>
    <Page class="page">
        <ActionBar class="action-bar">
            <Label class="label" text="Home"/>
        </ActionBar>

        <GridLayout columns="*, 2*, *" rows="*, 2*, *">
          <Button class="btn" col="0" row="0" text="Close"/>
          <Button class="btn" col="2" row="0" text="Add Count"/>

          <Button class="btn-primary btn-rounded-lg counter-adjust" col="0" row="1" text="-"/>
          <Label class="label counter-count" col="1" row="1" text="1000"/>
          <Button class="btn-primary btn-rounded-lg counter-adjust" col="2" row="1" text="+"/>

          <Button class="btn-primary btn-rounded-sm counter-reset" col="1" row="2" text="Reset"/>
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
    // Custom styles
    .counter-count {
      font-size: 62em;
    }

    .counter-adjust {
      font-size: 30em;
      margin: 100 16;
    }

    .counter-reset {
      font-size: 20em;
      margin: 30 15;
    }
</style>
