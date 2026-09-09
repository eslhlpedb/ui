---
title: Dialog
description: A window overlaid on either the primary window or another dialog window, rendering the content underneath inert.
featured: true
component: true
links:
  doc: https://www.radix-ui.com/docs/primitives/components/dialog
  api: https://www.radix-ui.com/docs/primitives/components/dialog#api-reference
---

<ComponentPreview name="dialog-demo" />

## Installation

<Tabs defaultValue="cli">

<TabsList>
  <TabsTrigger value="cli">CLI</TabsTrigger>
  <TabsTrigger value="manual">Manual</TabsTrigger>
</TabsList>

<TabsContent value="cli">

```bash
npx shadcn@latest add dialog
```

</TabsContent>

<TabsContent value="manual">

<Steps>

<Step>Install the following dependencies:</Step>

```bash
npm install @radix-ui/react-dialog
```

<Step>Copy and paste the following code into your project.</Step>

<ComponentSource name="dialog" />

<Step>Update the import paths to match your project setup.</Step>

</Steps>

</TabsContent>

</Tabs>

## Usage

```tsx
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from "@/components/ui/dialog"
```

```tsx
<Dialog>
  <DialogTrigger>Open</DialogTrigger>
  <DialogContent>
    <DialogHeader>
      <DialogTitle>Are you absolutely sure?</DialogTitle>
      <DialogDescription>
        This action cannot be undone. This will permanently delete your account
        and remove your data from our servers.
      </DialogDescription>
    </DialogHeader>
  </DialogContent>
</Dialog>
```

## Accessibility

Adheres to the [WAI-ARIA Dialog (Modal) Pattern](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/).

> **Note:** Every `DialogContent` must include a `DialogTitle` to ensure accessible announcements for screen readers. If a visible title isn't desired, wrap `DialogTitle` with a visually hidden class like `sr-only`.

### Keyboard Interactions

| Key | Description |
| --- | --- |
| `<kbd>Tab</kbd>` | Moves focus to the next focusable element within the dialog. |
| `<kbd>Shift</kbd> + <kbd>Tab</kbd>` | Moves focus to the previous focusable element within the dialog. |
| `<kbd>Esc</kbd>` | Closes the dialog and returns focus to the trigger element. |
| `<kbd>Space</kbd>` | Activates the trigger when focused. |
| `<kbd>Enter</kbd>` | Activates the trigger when focused. |