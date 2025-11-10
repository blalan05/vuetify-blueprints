<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-autocomplete label="Components" :items="['Alert', 'Appbar', 'Autocomplete', 'Avatar', 'Badge', 'Banner', 'Bottom Navigation', 'Bottom Sheet', 'Breadcrumbs', 'Button', 'Button Toggle']" v-model="components" multiple chips />
        </v-col>
        <v-col cols="12">
          <v-autocomplete label="Blueprints" :items="['MD1', 'MD2', 'MD3', 'Carbon', 'Spectrum', 'Bootstrap']" v-model="blueprints" />
        </v-col>
      </v-row>
      <md1Components :components="components" v-if="blueprints == 'MD1'" />
      <md2Components :components="components" v-if="blueprints == 'MD2'" />
      <md3Components :components="components" v-if="blueprints == 'MD3'" />
      <spectrumComponents :components="components" v-if="blueprints == 'Spectrum'" />
      <bootstrapComponents :components="components" v-if="blueprints == 'Bootstrap'" />
    </v-container>
  </v-app>
</template>
<script setup>
import { ref } from 'vue';
import md1Components from './md1Components.vue';
import md2Components from './md2Components.vue';
import md3Components from './md3Components.vue';
import spectrumComponents from './spectrumComponents.vue';
import bootstrapComponents from './bootstrapComponents.vue';

const components = ref(['Alert', 'Appbar', 'Autocomplete', 'Avatar', 'Badge', 'Banner', 'Bottom Navigation', 'Bottom Sheet', 'Breadcrumbs', 'Button', 'Button Toggle']);
const blueprints = ref('MD3')

</script>
