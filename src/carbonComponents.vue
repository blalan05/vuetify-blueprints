<template>
  <v-defaults-provider :defaults="blueprint">
  <v-row v-if="components.includes('Alert')">
      <v-col cols="12">
        <div class="text-h4">
          Alert
        </div>
        <v-alert title="Alert" text="This is a standard alert message." />
        <br />
        <v-alert title="Alert" text="This alert can be closed." closable />
        <br />
        <v-alert title="Alert" text="This alert has an icon." icon="$vuetify"/>
      </v-col>
    </v-row>
    <v-row v-if="components.includes('Badge')">
      <v-col cols="12">
        <div class="text-h4">
          Badge
        </div>
        <v-badge location="top right" color="error" content="1">
          <v-icon icon="mdi-cog"></v-icon>
        </v-badge>
        <v-badge location="bottom right" color="success" content="5">
          <v-icon icon="mdi-email"></v-icon>
        </v-badge>
        <v-badge color="info" content="99+">
          <v-btn>Notifications</v-btn>
        </v-badge>
      </v-col>
    </v-row>
  <v-row v-if="components.includes('Breadcrumbs')">
    <v-col cols="12">
      <div class="text-h4">
        Breadcrumbs
      </div>
      <v-breadcrumbs :items="breadcrumbItems"></v-breadcrumbs>
      <br />
      <v-breadcrumbs :items="breadcrumbItems" divider=">"></v-breadcrumbs>
      <br />
      <v-breadcrumbs :items="breadcrumbItems" color="primary"></v-breadcrumbs>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Button')">
    <v-col cols="12">
      <div class="text-h4">
        Button
      </div>
      <v-btn>Default</v-btn>
      <v-btn color="primary">Primary</v-btn>
      <v-btn color="secondary">Secondary</v-btn>
      <v-btn variant="outlined">Outlined</v-btn>
      <v-btn variant="text">Text</v-btn>
      <v-btn variant="plain">Plain</v-btn>
      <br /><br />
      <v-btn prepend-icon="mdi-plus">With Icon</v-btn>
      <v-btn append-icon="mdi-arrow-right">Append Icon</v-btn>
      <v-btn icon="mdi-heart"></v-btn>
      <br /><br />
      <v-btn size="small">Small</v-btn>
      <v-btn>Default</v-btn>
      <v-btn size="large">Large</v-btn>
      <v-btn size="x-large">X-Large</v-btn>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Button Toggle') || components.includes('Content Switch')">
    <v-col cols="12">
      <div class="text-h4">
        Button Toggle / Content Switch
      </div>
      <v-btn-toggle v-model="toggleValue" mandatory>
        <v-btn value="left">
          <v-icon start>mdi-format-align-left</v-icon>
          Left
        </v-btn>
        <v-btn value="center">
          <v-icon start>mdi-format-align-center</v-icon>
          Center
        </v-btn>
        <v-btn value="right">
          <v-icon start>mdi-format-align-right</v-icon>
          Right
        </v-btn>
      </v-btn-toggle>
      <br /><br />
      <v-btn-toggle v-model="toggleValue2" variant="outlined" mandatory>
        <v-btn value="bold">
          <v-icon>mdi-format-bold</v-icon>
        </v-btn>
        <v-btn value="italic">
          <v-icon>mdi-format-italic</v-icon>
        </v-btn>
        <v-btn value="underline">
          <v-icon>mdi-format-underline</v-icon>
        </v-btn>
      </v-btn-toggle>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Card')">
    <v-col cols="12">
      <div class="text-h4">
        Card
      </div>
      <v-card max-width="400">
        <v-card-title>Card Title</v-card-title>
        <v-card-subtitle>Card Subtitle</v-card-subtitle>
        <v-card-text>
          This is the card content. It can contain any text or components.
        </v-card-text>
        <v-card-actions>
          <v-btn>Action</v-btn>
          <v-spacer></v-spacer>
          <v-btn>Cancel</v-btn>
        </v-card-actions>
      </v-card>
      <br />
      <v-card max-width="400" variant="outlined">
        <v-card-title>Outlined Card</v-card-title>
        <v-card-text>
          This is an outlined card variant.
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Checkbox')">
    <v-col cols="12">
      <div class="text-h4">
        Checkbox
      </div>
      <v-checkbox label="Checkbox option 1" v-model="checkbox1"></v-checkbox>
      <v-checkbox label="Checkbox option 2" v-model="checkbox2"></v-checkbox>
      <v-checkbox label="Disabled checkbox" disabled></v-checkbox>
      <v-checkbox label="Indeterminate" indeterminate v-model="checkboxIndeterminate"></v-checkbox>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Chip')">
    <v-col cols="12">
      <div class="text-h4">
        Chip
      </div>
      <v-chip>Default Chip</v-chip>
      <v-chip color="primary">Primary Chip</v-chip>
      <v-chip color="secondary">Secondary Chip</v-chip>
      <v-chip closable>Closable Chip</v-chip>
      <v-chip prepend-icon="mdi-check">With Icon</v-chip>
      <v-chip variant="outlined">Outlined Chip</v-chip>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Dialog')">
    <v-col cols="12">
      <div class="text-h4">
        Dialog
      </div>
      <v-btn @click="dialog = true">Open Dialog</v-btn>
      <v-dialog v-model="dialog" max-width="500">
        <v-card>
          <v-card-title>Dialog Title</v-card-title>
          <v-card-text>
            This is the dialog content. You can add any content here.
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn @click="dialog = false">Close</v-btn>
            <v-btn color="primary" @click="dialog = false">Save</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('List')">
    <v-col cols="12">
      <div class="text-h4">
        List
      </div>
      <v-list>
        <v-list-item title="List Item 1" subtitle="Subtitle text"></v-list-item>
        <v-list-item title="List Item 2" subtitle="Subtitle text"></v-list-item>
        <v-list-item title="List Item 3" subtitle="Subtitle text"></v-list-item>
      </v-list>
      <br />
      <v-list>
        <v-list-item prepend-icon="mdi-email" title="Email" subtitle="email@example.com"></v-list-item>
        <v-list-item prepend-icon="mdi-phone" title="Phone" subtitle="+1 234 567 8900"></v-list-item>
        <v-list-item prepend-icon="mdi-map-marker" title="Location" subtitle="123 Main St"></v-list-item>
      </v-list>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Menu')">
    <v-col cols="12">
      <div class="text-h4">
        Menu
      </div>
      <v-menu>
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props">Open Menu</v-btn>
        </template>
        <v-list>
          <v-list-item title="Menu Item 1"></v-list-item>
          <v-list-item title="Menu Item 2"></v-list-item>
          <v-list-item title="Menu Item 3"></v-list-item>
        </v-list>
      </v-menu>
      <v-menu>
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props" icon="mdi-dots-vertical"></v-btn>
        </template>
        <v-list>
          <v-list-item prepend-icon="mdi-pencil" title="Edit"></v-list-item>
          <v-list-item prepend-icon="mdi-delete" title="Delete"></v-list-item>
        </v-list>
      </v-menu>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Pagination')">
    <v-col cols="12">
      <div class="text-h4">
        Pagination
      </div>
      <v-pagination v-model="page" :length="10"></v-pagination>
      <br />
      <v-pagination v-model="page2" :length="5" total-visible="7"></v-pagination>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Progress') || components.includes('Inline Loading')">
    <v-col cols="12">
      <div class="text-h4">
        Progress / Inline Loading
      </div>
      <v-progress-linear model-value="45"></v-progress-linear>
      <br />
      <v-progress-linear color="primary" model-value="75" buffer-value="90"></v-progress-linear>
      <br />
      <v-progress-circular model-value="60" color="primary"></v-progress-circular>
      <v-progress-circular indeterminate color="secondary"></v-progress-circular>
      <br /><br />
      <v-progress-circular indeterminate color="primary" size="20"></v-progress-circular>
      <span style="margin-left: 8px;">Loading...</span>
      <br /><br />
      <v-progress-circular indeterminate color="secondary" size="24"></v-progress-circular>
      <span style="margin-left: 8px;">Processing data...</span>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Radio')">
    <v-col cols="12">
      <div class="text-h4">
        Radio
      </div>
      <v-radio-group v-model="radioValue">
        <v-radio label="Option 1" value="1"></v-radio>
        <v-radio label="Option 2" value="2"></v-radio>
        <v-radio label="Option 3" value="3"></v-radio>
      </v-radio-group>
      <v-radio-group v-model="radioValue2" inline>
        <v-radio label="Inline 1" value="a"></v-radio>
        <v-radio label="Inline 2" value="b"></v-radio>
        <v-radio label="Inline 3" value="c"></v-radio>
      </v-radio-group>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Select')">
    <v-col cols="12">
      <div class="text-h4">
        Select
      </div>
      <v-select label="Select option" :items="['Option 1', 'Option 2', 'Option 3', 'Option 4']"></v-select>
      <br />
      <v-select label="Multiple selection" :items="['Item 1', 'Item 2', 'Item 3', 'Item 4']" multiple chips></v-select>
      <br />
      <v-select label="With prepend icon" :items="['Item 1', 'Item 2', 'Item 3']" prepend-icon="mdi-account"></v-select>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Slider')">
    <v-col cols="12">
      <div class="text-h4">
        Slider
      </div>
      <v-slider v-model="sliderValue" min="0" max="100"></v-slider>
      <br />
      <v-slider v-model="sliderValue2" min="0" max="100" step="10" show-ticks="always"></v-slider>
      <br />
      <v-range-slider v-model="rangeValue" min="0" max="100"></v-range-slider>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Switch')">
    <v-col cols="12">
      <div class="text-h4">
        Switch
      </div>
      <v-switch label="Switch option 1" v-model="switch1"></v-switch>
      <v-switch label="Switch option 2" v-model="switch2" color="primary"></v-switch>
      <v-switch label="Disabled switch" disabled></v-switch>
      <v-switch label="Switch with icon" prepend-icon="mdi-wifi" v-model="switch3"></v-switch>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Table')">
    <v-col cols="12">
      <div class="text-h4">
        Table
      </div>
      <v-table>
        <thead>
          <tr>
            <th>Name</th>
            <th>Email</th>
            <th>Role</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>John Doe</td>
            <td>john@example.com</td>
            <td>Admin</td>
          </tr>
          <tr>
            <td>Jane Smith</td>
            <td>jane@example.com</td>
            <td>User</td>
          </tr>
          <tr>
            <td>Bob Johnson</td>
            <td>bob@example.com</td>
            <td>User</td>
          </tr>
        </tbody>
      </v-table>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Tabs')">
    <v-col cols="12">
      <div class="text-h4">
        Tabs
      </div>
      <v-tabs v-model="tab">
        <v-tab value="one">Tab One</v-tab>
        <v-tab value="two">Tab Two</v-tab>
        <v-tab value="three">Tab Three</v-tab>
      </v-tabs>
      <v-window v-model="tab">
        <v-window-item value="one">Content for Tab One</v-window-item>
        <v-window-item value="two">Content for Tab Two</v-window-item>
        <v-window-item value="three">Content for Tab Three</v-window-item>
      </v-window>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Text Field')">
    <v-col cols="12">
      <div class="text-h4">
        Text Field
      </div>
      <v-text-field label="Standard"></v-text-field>
      <v-text-field label="With hint" hint="This is a hint"></v-text-field>
      <v-text-field label="With prepend icon" prepend-icon="mdi-account"></v-text-field>
      <v-text-field label="Password" type="password" prepend-icon="mdi-lock"></v-text-field>
      <v-text-field label="Error state" error-messages="This field has an error"></v-text-field>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Textarea')">
    <v-col cols="12">
      <div class="text-h4">
        Textarea
      </div>
      <v-textarea label="Textarea"></v-textarea>
      <v-textarea label="With hint" hint="Enter your message here"></v-textarea>
      <v-textarea label="Auto-grow" auto-grow></v-textarea>
      <v-textarea label="With counter" counter maxlength="100"></v-textarea>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Tooltip')">
    <v-col cols="12">
      <div class="text-h4">
        Tooltip
      </div>
      <v-tooltip>
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props">Hover me</v-btn>
        </template>
        <span>This is a tooltip</span>
      </v-tooltip>
      <v-tooltip location="top">
        <template v-slot:activator="{ props }">
          <v-btn v-bind="props" icon="mdi-help-circle"></v-btn>
        </template>
        <span>Help tooltip</span>
      </v-tooltip>
      <v-tooltip location="bottom">
        <template v-slot:activator="{ props }">
          <v-icon v-bind="props" icon="mdi-information"></v-icon>
        </template>
        <span>Information tooltip</span>
      </v-tooltip>
    </v-col>
  </v-row>
  <v-row v-if="components.includes('Treeview')">
    <v-col cols="12">
      <div class="text-h4">
        Treeview
      </div>
      <v-treeview :items="treeviewItems"></v-treeview>
      <br />
      <v-treeview :items="treeviewItems" activatable item-title="title" item-children="children"></v-treeview>
    </v-col>
  </v-row>
  </v-defaults-provider>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps<{
  components: string[]
}>()

const dialog = ref(false)
const checkbox1 = ref(false)
const checkbox2 = ref(false)
const checkboxIndeterminate = ref(false)
const page = ref(1)
const page2 = ref(1)
const radioValue = ref('1')
const radioValue2 = ref('a')
const sliderValue = ref(50)
const sliderValue2 = ref(30)
const rangeValue = ref([20, 80])
const switch1 = ref(false)
const switch2 = ref(true)
const switch3 = ref(false)
const tab = ref('one')
const toggleValue = ref('left')
const toggleValue2 = ref('bold')

const breadcrumbItems = [
  {
    title: 'Home',
    disabled: false,
    href: '#',
  },
  {
    title: 'Category',
    disabled: false,
    href: '#',
  },
  {
    title: 'Subcategory',
    disabled: true,
    href: '#',
  },
]

const treeviewItems = [
  {
    id: 1,
    title: 'Applications',
    children: [
      { id: 2, title: 'Calendar' },
      { id: 3, title: 'Chrome' },
      { id: 4, title: 'Webstorm' },
    ],
  },
  {
    id: 5,
    title: 'Documents',
    children: [
      {
        id: 6,
        title: 'Vuetify',
        children: [
          { id: 7, title: 'src' },
          { id: 8, title: 'test' },
        ],
      },
      {
        id: 9,
        title: 'Material Design',
        children: [
          { id: 10, title: 'src' },
          { id: 11, title: 'plugins' },
        ],
      },
    ],
  },
]

const blueprint = {
  VBtn: {
    color: 'primary',
  },
  VSelect: {
    variant: 'outlined',
  },
  VSlider: {
    color: 'primary',
  },
  VTabs: {
    color: 'primary',
  },
  VTextarea: {
    variant: 'outlined',
  },
  VTextField: {
    variant: 'outlined',
  },
}
</script>
