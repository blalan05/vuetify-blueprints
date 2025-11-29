# Design System Component Comparison

This document compares components across different design systems to identify common components that can be showcased.

## Component Lists by Design System

### Material Design 1 (MD1)
- Alert
- App Bar
- Autocomplete
- Avatar
- Badge
- Banner
- Bottom Navigation
- Bottom Sheet
- Breadcrumbs
- Button
- Button Toggle
- Card
- Checkbox
- Chip
- Date Picker
- Dialog
- Divider
- Expansion Panel
- Floating Action Button
- List
- Menu
- Navigation Drawer
- Pagination
- Progress Indicator
- Radio Button
- Select
- Slider
- Snackbar
- Switch
- Table
- Tabs
- Text Field
- Textarea
- Time Picker
- Tooltip

### Material Design 2 (MD2)
- Alert
- App Bar
- Autocomplete
- Avatar
- Badge
- Banner
- Bottom Navigation
- Bottom Sheet
- Breadcrumbs
- Button
- Button Toggle
- Card
- Checkbox
- Chip
- Date Picker
- Dialog
- Divider
- Expansion Panel
- Floating Action Button
- List
- Menu
- Navigation Drawer
- Pagination
- Progress Indicator
- Radio Button
- Select
- Slider
- Snackbar
- Switch
- Table
- Tabs
- Text Field
- Textarea
- Time Picker
- Tooltip

### Material Design 3 (MD3)
- Alert
- App Bar
- Autocomplete
- Avatar
- Badge
- Banner
- Bottom Navigation
- Bottom Sheet
- Breadcrumbs
- Button
- Button Toggle
- Card
- Checkbox
- Chip
- Date Picker
- Dialog
- Divider
- Expansion Panel
- Floating Action Button
- List
- Menu
- Navigation Drawer
- Pagination
- Progress Indicator
- Radio Button
- Select
- Slider
- Snackbar
- Switch
- Table
- Tabs
- Text Field
- Textarea
- Time Picker
- Tooltip

### IBM Carbon Design System
- Accordion
- Alert
- Badge
- Breadcrumb
- Button
- Button Set
- Checkbox
- Code Snippet
- ComboBox
- Content Switcher
- Data Table
- Date Picker
- Dropdown
- File Uploader
- Form
- Inline Loading
- Link
- List
- Loading
- Modal
- Notification
- Number Input
- Overflow Menu
- Pagination
- Progress Indicator
- Radio Button
- Search
- Select
- Slider
- Structured List
- Tabs
- Tag
- Text Area
- Text Input
- Toggle
- Tooltip
- Tree View
- UI Shell Header
- UI Shell Left Panel

### Adobe Spectrum Design System
- Action Button
- Action Group
- Alert Dialog
- Avatar
- Badge
- Banner
- Breadcrumbs
- Button
- Calendar
- Checkbox
- Coach Mark
- Color Area
- Color Field
- Color Loupe
- Color Slider
- Color Wheel
- Combo Box
- Date Picker
- Dialog
- Divider
- Drop Indicator
- Drop Zone
- Field Group
- Form
- Grid List
- Heading
- Help Text
- Icon
- Illustrated Message
- Image
- Inline Alert
- Link
- List Box
- Logic Button
- Menu
- Number Field
- Pagination
- Popover
- Progress Bar
- Radio
- Radio Group
- Slider
- Switch
- Table
- Tabs
- Tag
- Text Area
- Tray
- Text Field
- Toast
- Tooltip

### Bootstrap
- Accordion
- Alert
- Badge
- Breadcrumb
- Button
- Card
- Carousel
- Collapse
- Dropdown
- Form
- List Group
- Modal
- Navs
- Navbar
- Pagination
- Popover
- Progress
- Scrollspy
- Toast
- Tooltip
- Table

## Common Components Across All Systems

These components exist in all 6 design systems (MD1, MD2, MD3, Carbon, Spectrum, Bootstrap):

1. **Alert** - All systems have alert/notification components
2. **App Bar** - Top navigation/header bar (UI Shell Header in Carbon, Header in Spectrum, Navbar in Bootstrap)
3. **Badge** - Status indicators and notification badges
4. **Breadcrumbs** - Navigation breadcrumbs
5. **Button** - Primary action buttons (Action Button in Spectrum → Button)
6. **Button Toggle** - Toggle button groups (Content Switcher in Carbon, Action Group in Spectrum, Button Group in Bootstrap)
7. **Card** - Content containers (Tile in Carbon, Coach Mark in Spectrum)
8. **Chip/Tag** - Compact labels/tags (Tag in Carbon and Spectrum, Pill Badge in Bootstrap)
9. **Checkbox** - Form selection control
10. **Dialog/Modal** - Modal dialogs (called Modal in Bootstrap/Carbon, Dialog in others)
11. **List** - List components (List Group in Bootstrap, Structured List in Carbon → Table)
12. **Menu** - Dropdown menus and context menus (Dropdown in Bootstrap)
13. **Pagination** - Page navigation controls
14. **Progress Indicator** - Progress bars/indicators (Inline Loading in Carbon → Progress)
15. **Radio Button** - Single selection form control
16. **Select/Dropdown** - Dropdown selection (Dropdown in Carbon, Select/Picker in others)
17. **Slider** - Range slider input
18. **Switch/Toggle** - Toggle switch (Toggle in Carbon, Switch in others)
19. **Table** - Data tables (Structured List in Carbon → Table)
20. **Tabs** - Tab navigation
21. **Text Field/Input** - Text input fields
22. **Textarea** - Multi-line text input
23. **Tooltip** - Hover tooltips

## Components in Most Systems (1 component)
- **Navigation Drawer** - Present in MD1-3, Carbon (as UI Shell Left Panel), Spectrum (as Side Nav), Bootstrap (as Offcanvas)
- **Treeview** - Present in MD1-3, Carbon (via Tree View mapping)

## Components Unique to Specific Systems

### Material Design Only
- Autocomplete
- Avatar
- Banner
- Bottom Navigation
- Bottom Sheet (also in Spectrum as Tray)
- Date Picker
- Expansion Panel
- Floating Action Button
- Snackbar
- Time Picker

### Carbon Only
- Code Snippet
- File Uploader

**Note:** Carbon components mapped to common components:
- **Content Switcher** → Button Toggle
- **Inline Loading** → Progress Indicator
- **Overflow Menu** → Menu
- **Structured List** → Table
- **Tile** → Card
- **Tree View** → Treeview (also in MD1-3)
- **UI Shell Header** → App Bar
- **UI Shell Left Panel** → Navigation Drawer

### Spectrum Only
- Color Area/Field/Loupe/Slider/Wheel
- Drop Indicator
- Drop Zone
- Grid List
- Illustrated Message
- Logic Button
- Number Field
- Popover

**Note:** Spectrum components mapped to common components:
- **Action Button** → Button
- **Action Group** → Button Toggle
- **Coach Mark** → Card
- **Field Group** → Checkbox
- **Header** → App Bar
- **Meter** → Progress
- **Picker** → Select
- **Progress Circle** → Progress
- **Search Field** → Text Field
- **Side Nav** → Navigation Drawer
- **Status Light** → Chip
- **Tray** → Bottom Sheet
- **Well** → Card

**Note:** Modal Overlay in Spectrum is about dictating elevated content (elevation/styling system), not a unique component.

### Bootstrap Only
- Carousel
- Collapse
- Scrollspy

**Note:** Bootstrap components mapped to common components:
- **Button Group** → Button Toggle
- **Dropdown** → Menu
- **Input Group** → Text Field
- **Navbar** → App Bar
- **Offcanvas** → Navigation Drawer
- **Pill Badge** → Chip
- **Spinner** → Progress

## Recommended Components to Showcase

Based on this comparison, here are the components that should be showcased:

### Tier 1: Common to All Systems (23 components)
1. Alert
2. App Bar (also in Carbon as UI Shell Header, Spectrum as Header, Bootstrap as Navbar)
3. Badge
4. Breadcrumbs
5. Button
6. Button Toggle (also in Carbon as Content Switcher, Spectrum as Action Group, Bootstrap as Button Group)
7. Card (also in Carbon as Tile, Spectrum as Coach Mark)
8. Chip/Tag (also in Carbon as Tag, Spectrum as Tag, Bootstrap as Pill Badge)
9. Checkbox
10. Dialog/Modal
11. List
12. Menu (also in Bootstrap as Dropdown)
13. Pagination
14. Progress Indicator
15. Radio Button
16. Select/Dropdown
17. Slider
18. Switch/Toggle
19. Table
20. Tabs
21. Text Field/Input
22. Textarea
23. Tooltip

### Tier 2: Common to Most Systems (1 component)
22. Navigation Drawer (also in Carbon as UI Shell Left Panel, Spectrum as Side Nav, Bootstrap as Offcanvas)

### Tier 3: Material Design Specific (can show MD1-3 only)
24. Autocomplete
25. Avatar
26. Banner
27. Bottom Navigation
28. Bottom Sheet (also in Spectrum as Tray)
29. Date Picker
30. Expansion Panel
31. Floating Action Button
32. Snackbar
33. Time Picker
34. Treeview (also in Carbon as Tree View)

## Component Mappings

Design systems often use different names for similar components. Here are the mappings we use:

### Carbon Design System Mappings
- **Content Switcher** → Button Toggle
- **Inline Loading** → Progress Indicator
- **Overflow Menu** → Menu
- **Structured List** → Table
- **Tile** → Card
- **Tree View** → Treeview
- **UI Shell Header** → App Bar
- **UI Shell Left Panel** → Navigation Drawer

### Spectrum Design System Mappings
- **Action Button** → Button
- **Action Group** → Button Toggle
- **Coach Mark** → Card
- **Field Group** → Checkbox
- **Header** → App Bar
- **Meter** → Progress
- **Picker** → Select
- **Progress Circle** → Progress
- **Search Field** → Text Field
- **Side Nav** → Navigation Drawer
- **Status Light** → Chip
- **Tray** → Bottom Sheet
- **Well** → Card

**Note:** Modal Overlay in Spectrum is about dictating elevated content (elevation/styling system), not a unique component.

### Bootstrap Design System Mappings
- **Button Group** → Button Toggle
- **Dropdown** → Menu
- **Input Group** → Text Field
- **Navbar** → App Bar
- **Offcanvas** → Navigation Drawer
- **Pill Badge** → Chip
- **Spinner** → Progress

These mappings allow us to showcase components across design systems using a common component name, while still demonstrating how each system styles them.

## Implementation Strategy

1. **Show all Tier 1 components** for all 6 design systems
2. **Show Tier 2 components** for systems that support them (with notes where missing)
3. **Show Tier 3 components** only for MD1, MD2, MD3 blueprints
4. **Map design-system-specific component names** to common component names (see Component Mappings above)
5. Add a note/indicator when a component is not available in a specific design system

