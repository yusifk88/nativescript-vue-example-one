<template>
  <Page>
    <ActionBar :title="item.title"/>

    <ScrollView height="100%">

      <StackLayout>
        <Image margin="0" stretch="aspectFill" :src="item.image"></Image>

        <StackLayout
            padding="10 20"
        >
          <StackLayout v-for="detail in item.details" :key="detail.id">
            <Label
            marginTop="15"
            fontSize="16"
            fontWeight="700"
            class="text-primary"
            textWrap="true"
            :text="detail.title"
            />

            <Label
              fontSize="14"
              class="text-primary"
              textWrap="true"
              :text="detail.body"

            />

          </StackLayout>

        </StackLayout>
      </StackLayout>

    </ScrollView>
  </Page>
</template>

<script>
import Vue from 'nativescript-vue'

export default Vue.extend({
  props: ['item'],
  name: "Details"
})
</script>


<style scoped lang="scss">

</style>
