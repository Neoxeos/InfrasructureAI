## Goal

Build `editor` home screen and project dialog/sidebar actions. No api calls yet

## Editor Home

Reuse the existing editor layour. Do not ,odify the navbar or sidebar editor

In teh center of the page, add:

- heading `Create a project or open an existing one`
- description: `Start new architecture workspace, or choose a project from sidebar.`
- `New Project` button with a `Plus` icon

keep the layout minimal, Do not wrap this content in cards

Clicking `New Project` should open the Create Project dialog.

## Dialogs

### Create Project

- project name input
- live slug preview on the name
- preview updates as user types

### Rename project

- prefiled project name input
- current project name shown in description
- input auto-focuses
- Enter submits

### Delete Project

- destructive confirmation only
- no input
- confirm button uses destructive styling

## Sidebar

Add project item Actions:

- rename 
- delete

show actions only for owned proejcts

hide actions for shared/collaborator projects

on mobile:

- tapping outside the sidebar closes it
- add a backdrop scrim

## Implementation

Create dedicated hook to manage:

- dialog state
- form state
- loading state

Wire:

- editor home `New Project` -> Createe dialog
- sidebar create -> Create dialog
- sidebar rename -> Rename dialog
- sidebar delete -> Delete dialog

Use mock project data only. Do not add API calls or persistence.

## Cehck when done

- sidebar actions are wired
- slug preview works
- no Typescript errors
- no lint errors