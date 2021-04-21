<template>
    <Page class="page">
        <ActionBar class="action-bar">
            <Label class="label" text="Home"/>
        </ActionBar>

        <GridLayout columns="*, 2*, *" rows="*, 2*, *">
          <!-- decrement -->
          <Button class="btn-primary btn-rounded-lg counter-adjust" col="0" row="1" @tap="decrement" text.decode="&#x2193;"/>
          <!-- the count -->
          <Label class="label counter-count" col="1" row="1" :text="viewableCount"/>
          <!-- increment -->
          <Button class="btn-primary btn-rounded-lg counter-adjust" col="2" row="1" @tap="increment" text.decode="&#x2191;"/>

          <!-- reset -->
          <Button class="btn-primary btn-rounded-sm counter-reset" col="1" row="2" @tap="reset" text="Reset"/>
        </GridLayout>
    </Page>
</template>

<script>
  export default {
    data() {
      return {
        count: 0
      }
    },
    methods: {
      increment() {
        this.count = this.count + 1;
      },
      decrement() {
        // constraint on going negative (don't do it)
        if (this.count == 0) {
          return;
        }

        this.count = this.count - 1;
      },
      reset() {
        this.count = 0;
      }
    },
    computed: {
      viewableCount() {
        return this.count.toString();
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
