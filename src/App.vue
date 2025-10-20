<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-autocomplete label="Components" :items="['Alert', 'Appbar', 'Autocomplete', 'Avatar', 'Badge', 'Banner', 'Bottom Navigation', 'Bottom Sheet', 'Breadcrumbs', 'Button', 'Button Toggle']" v-model="components" multiple chips />
        </v-col>
        <v-col cols="12">
          <v-autocomplete label="Blueprints" :items="['MD1', 'MD2', 'MD3', 'Carbon', 'Spectrum', 'Bootstrap']" v-model="blueprints" disabled />
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Alert')">
        <v-col cols="12">
          <div class="text-h4">
            Alert
          </div>
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." closable />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." icon="$vuetify"/>
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." closable icon="$vuetify" />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." border="start" />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." border="top" />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." border="end" />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." border="bottom" />
          <br />
          <v-alert title="Alert" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl.  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl eget aliquam aliquet, nisl nisl aliquet nisl, eget aliquam nisl nisl eget nisl." border="start" variant="outlined" />
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Appbar')">
        <v-col>
          <div class="text-h4">
            Appbar
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Autocomplete')">
        <v-col>
          <div class="text-h4">
            Autocomplete
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Avatar')">
        <v-col>
          <div class="text-h4">
            Avatar
          </div>
          <v-avatar icon="$vuetify" size="44" />
          <br></br>
          <v-avatar size="44" />
          <br/>
          <v-avatar color="surface-variant" size="44">44</v-avatar>
          <br></br>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Badge')">
        <v-col>
          <div class="text-h4">
            Badge
          </div>
          <v-container>
            <v-row>
              <v-badge location="top right" color="error" content="1">
                <v-icon icon="mdi-cog"></v-icon>
              </v-badge>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Banner')">
        <v-col>
          <div class="text-h4">
            Banner
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Bottom Navigation')">
        <v-col>
          <div class="text-h4">
            Bottom Navigation
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Bottom Sheet')">
        <v-col>
          <div class="text-h4">
            Bottom Sheet
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Breadcrumbs')">
        <v-col>
          <div class="text-h4">
            Breadcrumbs
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Button')">
        <v-col>
          <div class="text-h4">
            Button
          </div>
        </v-col>
      </v-row>
      <v-row v-if="components.includes('Button Toggle')">
        <v-col>
          <div class="text-h4">
            Button Toggle
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script setup>
import { ref } from 'vue';

const components = ref(['Alert', 'Appbar', 'Autocomplete', 'Avatar', 'Badge', 'Banner', 'Bottom Navigation', 'Bottom Sheet', 'Breadcrumbs', 'Button', 'Button Toggle']);
const blueprints = ['MD3']

</script>
