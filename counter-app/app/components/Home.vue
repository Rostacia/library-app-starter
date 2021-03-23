<template>
    <Page>
        <ActionBar>
            <Label text="Home"/>
        </ActionBar>

        <GridLayout columns="1*, 3*, 1*" rows="4*, 3*, 2*">
            <Label class="info" row="0" col="1" text="Count goes here"></Label>
            <Label row="=1" col="0">
              <FormattedString>
                <Span class="far" text="&plus;"></Span>
              </FormattedString>
            </Label>
            <Label row="=1" col="2">
              <FormattedString>
                <Span class="far" text="&minus;"></Span>
              </FormattedString>
            </Label>
            <Label row="2" col="1">
              <FormattedString>
                <Span class="far" text="&spin;"></Span>
              </FormattedString>
              <Button text="Reset"></Button>
            </Label>
        </GridLayout>
    </Page>
</template>

<script>
  export default {
    computed: {
      message() {
        return "Blank {N}-Vue app";
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

    .info {
        font-size: 20;
        horizontal-align: center;
        vertical-align: center;
    }
</style>
