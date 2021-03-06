# UIKit | Dialogs

## UIAlert

```typescript
/**
 * Returns an UIAlert instance with specific message and button-title text.
 */
constructor(message: string, buttonText: string = "OK")

/**
 * Shows the dialog, callback will be called after button taps.
 */
show(completed: () => void): void
```

## UIPrompt

```typescript
/**
 * Returns an UIPrompt instance with specific message.
 */
constructor(message: string)

/**
 * The confirm button-title text displayed in the dialog.
 */
confirmTitle: string = "Done"

/**
 * The cancel button-title text displayed in the dialog.
 */
cancelTitle: string = "Cancel"

/**
 * The text-field placeholder text displayed in the dialog.
 */
placeholder: string

/**
 * The text-field default text displayed in the dialog.
 */
defaultValue: string

/**
 * Shows the dialog, completed callback will be called after confirm button taps, calcelled callback will be called after cancel button taps.
 */
show(completed: (text: string) => void, cancelled?: () => void): void
```

## UIConfirm

```typescript
/**
 * Returns an UIConfirm instance with specific message.
 */
constructor(message: string)

/**
 * The confirm button-title text displayed in the dialog.
 */
confirmTitle: string = "Yes"

/**
 * The cancel button-title text displayed in the dialog.
 */
cancelTitle: string = "No"

/**
 * Shows the dialog, completed callback will be called after confirm button taps, calcelled callback will be called after cancel button taps.
 */
show(completed?: () => void, cancelled?: () => void): void
```

## UIActionSheet

```typescript

/**
 * The message text at top.
 */
message: string

/**
 * Add regular action button to actionsheet.
 */
addRegularAction(title: string, acitonBlock:() => void): void

/**
 * Add danegr action (red title) button to actionsheet.
 */
addDangerAction(title: string, acitonBlock:() => void): void

/**
 * Add cancel action button to actionsheet.
 */
addCancelAction(title: string, acitonBlock:() => void): void

/**
 * Shows the dialog.
 */
show(): void
```

## UIMenu

```typescript

/**
 * Add menu item with action to menu controller.
 */
addMenuItem(title: string, actionBlock:() => void): void

/**
 * Shows the menu.
 */
show(inView: UIView): void

```