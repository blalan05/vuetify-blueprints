<template>
  <v-dialog v-model="model" fullscreen>
    <v-card>
      <v-toolbar>
        <v-toolbar-title>Component Comparison</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon @click="model = false">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-toolbar>
      <v-card-text>
        <v-table>
          <thead>
            <tr>
              <th>Component</th>
              <th>MD1</th>
              <th>MD2</th>
              <th>MD3</th>
              <th>Carbon</th>
              <th>Spectrum</th>
              <th>Bootstrap</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="component in components" :key="component.name">
              <td><strong>{{ component.name }}</strong></td>
              <td class="text-center">
                <v-icon v-if="component.md1" color="success">mdi-check</v-icon>
                <span v-else>-</span>
              </td>
              <td class="text-center">
                <v-icon v-if="component.md2" color="success">mdi-check</v-icon>
                <span v-else>-</span>
              </td>
              <td class="text-center">
                <v-icon v-if="component.md3" color="success">mdi-check</v-icon>
                <span v-else>-</span>
              </td>
              <td class="text-center">
                <v-icon v-if="component.carbon" color="success">mdi-check</v-icon>
                <v-chip v-else-if="component.carbonMapped" size="small" variant="outlined" color="info">Mapped</v-chip>
                <span v-else>-</span>
              </td>
              <td class="text-center">
                <v-icon v-if="component.spectrum" color="success">mdi-check</v-icon>
                <v-chip v-else-if="component.spectrumMapped" size="small" variant="outlined" color="info">Mapped</v-chip>
                <span v-else>-</span>
              </td>
              <td class="text-center">
                <v-icon v-if="component.bootstrap" color="success">mdi-check</v-icon>
                <v-chip v-else-if="component.bootstrapMapped" size="small" variant="outlined" color="info">Mapped</v-chip>
                <span v-else>-</span>
              </td>
            </tr>
          </tbody>
        </v-table>
        <v-alert type="info" class="mt-4">
          <strong>Legend:</strong>
          <ul class="mt-2">
            <li><v-icon size="small" color="success">mdi-check</v-icon> = Component has a spec in this design system</li>
            <li><v-chip size="small" variant="outlined" color="info">Mapped</v-chip> = Component mapped from design-system-specific name</li>
            <li>- = Component not available in this design system</li>
          </ul>
        </v-alert>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const props = defineProps<{
  modelValue: boolean
}>()

const emit = defineEmits<{
  'update:modelValue': [value: boolean]
}>()

const model = computed({
  get: () => props.modelValue,
  set: (value) => emit('update:modelValue', value)
})

const components = [
  // Tier 1 - Common to all
  { name: 'Alert', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'App Bar', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, spectrumMapped: true, bootstrap: true, bootstrapMapped: true },
  { name: 'Badge', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Breadcrumbs', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Button', md1: true, md2: true, md3: true, carbon: true, spectrum: true, spectrumMapped: true, bootstrap: true },
  { name: 'Button Toggle', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, spectrumMapped: true, bootstrap: true, bootstrapMapped: true },
  { name: 'Card', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, spectrumMapped: true, bootstrap: true },
  { name: 'Chip', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, spectrumMapped: true, bootstrap: true, bootstrapMapped: true },
  { name: 'Checkbox', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Dialog', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'List', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Menu', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true, bootstrapMapped: true },
  { name: 'Pagination', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Progress', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, bootstrap: true },
  { name: 'Radio', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Select', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Slider', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Switch', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Table', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, bootstrap: true },
  { name: 'Tabs', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Text Field', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Textarea', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  { name: 'Tooltip', md1: true, md2: true, md3: true, carbon: true, spectrum: true, bootstrap: true },
  // Tier 2 - Most systems
  { name: 'Navigation Drawer', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: true, spectrumMapped: true, bootstrap: true, bootstrapMapped: true },
  // Tier 3 - Material Design specific
  { name: 'Treeview', md1: true, md2: true, md3: true, carbon: true, carbonMapped: true, spectrum: false, bootstrap: false },
]
</script>

