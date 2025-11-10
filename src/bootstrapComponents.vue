<template>
  <v-row v-if="components.includes('Alert')">
    <v-defaults-provider :defaults="blueprint">
      <v-col>
        <div class="text-h4">
          Alert
        </div>
        <v-alert text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl."><v-btn>Click me</v-btn></v-alert>
        <br />
        <v-alert text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.">
          <template #close>
            <v-icon-btn>
              <v-icon icon="mdi-close" />
            </v-icon-btn>
          </template>
        </v-alert>
        <br />
        <v-alert text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." icon="$vuetify" />
      </v-col>
      </v-defaults-provider>
    </v-row>
  </template>
<script setup lang="ts">
const props = defineProps<{
  components: string[]
}>()

const blueprint = {
  VAlert: {
    class: 'pa-0',
    rounded: 'lg', // Not Correct lg -> 8px should be 6px
    variant: 'outlined',
    VIconBtn: {
      rounded: 'lg',
      class: 'px-4, py-5',
    }
  }
}
</script>