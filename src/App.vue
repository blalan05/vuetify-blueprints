<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12" class="d-flex align-center">
          <v-autocomplete label="Components" :items="['Alert', 'Badge', 'Breadcrumbs', 'Button', 'Button Toggle', 'Card', 'Checkbox', 'Chip', 'Dialog', 'List', 'Menu', 'Pagination', 'Progress', 'Radio', 'Select', 'Slider', 'Switch', 'Table', 'Tabs', 'Text Field', 'Textarea', 'Tooltip', 'Treeview']" v-model="components" multiple chips class="flex-grow-1" />
          <v-btn icon="mdi-information" variant="text" @click="showComparison = true" class="ml-2">
            <v-icon>mdi-information</v-icon>
            <v-tooltip activator="parent">Component Comparison</v-tooltip>
          </v-btn>
        </v-col>
        <v-col cols="12">
          <v-autocomplete label="Blueprints" :items="['MD1', 'MD2', 'MD3', 'Carbon', 'Spectrum', 'Bootstrap']" v-model="blueprints" />
        </v-col>
      </v-row>
      <md1Components :components="components" v-if="blueprints == 'MD1'" />
      <md2Components :components="components" v-if="blueprints == 'MD2'" />
      <md3Components :components="components" v-if="blueprints == 'MD3'" />
      <carbonComponents :components="components" v-if="blueprints == 'Carbon'" />
      <spectrumComponents :components="components" v-if="blueprints == 'Spectrum'" />
      <bootstrapComponents :components="components" v-if="blueprints == 'Bootstrap'" />
    </v-container>
    <ComponentComparison v-model="showComparison" />
  </v-app>
</template>
<script setup>
import { ref } from 'vue';
import md1Components from './md1Components.vue';
import md2Components from './md2Components.vue';
import md3Components from './md3Components.vue';
import carbonComponents from './carbonComponents.vue';
import spectrumComponents from './spectrumComponents.vue';
import bootstrapComponents from './bootstrapComponents.vue';
import ComponentComparison from './components/ComponentComparison.vue';

const components = ref(['Alert', 'Badge', 'Breadcrumbs', 'Button', 'Button Toggle', 'Card', 'Checkbox', 'Chip', 'Dialog', 'List', 'Menu', 'Pagination', 'Progress', 'Radio', 'Select', 'Slider', 'Switch', 'Table', 'Tabs', 'Text Field', 'Textarea', 'Tooltip', 'Treeview']);
const blueprints = ref('MD3')
const showComparison = ref(false)

</script>
