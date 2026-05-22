We need the base chrome compoents that frame every editor screen - the top navbar and the left sidebar shell. These will be reused and extended in every chapter that follows.

### Editor Navbar

Create `components/editor/editor-navbar.tsx`.

Requirements:

- fixed-height top navbar
- left, center and right sections
- left section contains sidebar toggle button
- use `PanelLeftOpen` / `PaneleLeftClose` icons based on sidebar state
- right section stays empty for now
- dark background with subtle buttom border


### Project Sidebar

Create `components/editor/project-sidebar.tsx`

Requierements:

- sidebar should float above editor canvas
- opening it should not push page content
- slides in from teh left
- accept `isOpen` prop and `onClose` prop
- header with `Projects` title + close button
- shadcn `Tabs`:
    - My Projects
    - Shared
- Both tabs show empty placeholder state
- full-width `New Project` button at the buttom with `Plus` icon

### Dialog Pattern

Use exisiting color tokens from `global.css` for dialog styling

Support:
- title
- description
- footer actions

Do no build actual dialogs yet.

### Check when done

- new components compile without TypeScript errors
- no lint errors
- dialog pattern is ready for future use