# UIKit | UIAttributedString

## UIAttributedString

A string that has associated attributes (such as visual style, hyperlinks, or accessibility data) for portions of its text.

```typescript
/**
 * Returns an UIAttributedString object initialized with a given string and attributes.
 */
constructor(str: string, attributes: {[key: string]: any})  // attributes -> key: UIAttributedStringKey

/**
 * Returns current UIAttributeString bounding rect in specific size.
 */
measure(inSize: Size): Rect

/**
 * Returns an UIMutableAttributedString object instance with this string and attributes.
 */
mutable(): UIMutableAttributedString
```

## UIMutableAttributedString extends UIAttributedString

```typescript
/**
 * Returns an UIMutableAttributedString object initialized with a given string and attributes.
 */
constructor(str: string, attributes: {[key: string]: any})  // attributes -> key: UIAttributedStringKey

/**
 * Replaces the characters in the given range with the characters of the given string.
 */
replaceCharacters(inRange: Range, withString: string): void

/**
 * Sets the attributes for the characters in the specified range to the specified attributes.
 */
setAttributes(attributes: {[key: string]: any}, range: Range): void

/**
 * Adds an attribute with the given name and value to the characters in the specified range.
 */
addAttribute(attrName: string, value: any, range: Range): void

/**
 * Adds the given collection of attributes to the characters in the specified range.
 */
addAttributes(attributes: {[key: string]: any}, range: Range): void

/**
 * Removes the named attribute from the characters in the specified range.
 */
removeAttribute(attrName: string, range: Range): void

/**
 * Replaces the characters and attributes in a given range with the characters and attributes of the given attributed string.
 */
replaceCharactersWithAttributedString(inRange: Range, withAttributedString: UIAttributedString): void

/**
 * Inserts the characters and attributes of the given attributed string into the receiver at the given index.
 */
insertAttributedString(attributedString: UIAttributedString, atIndex: number): void

/**
 * Adds the characters and attributes of a given attributed string to the end of the receiver.
 */
appendAttributedString(attributedString: UIAttributedString): void

/**
 * Deletes the characters in the given range along with their associated attributes.
 */
deleteCharacters(inRange: Range): void

/**
 * Returns an UIAttributedString object instance with this string and attributes.
 */
immutable(): UIAttributedString
```

## UIAttributedStringKey

```typescript

enum UIAttributedStringKey {
    foregroundColor,      // value: UIColor
    font,                 // value: UIFont
    backgroundColor,      // value: UIColor
    kern,                 // value: number
    strikethroughStyle,   // value: number
    underlineStyle,       // value: number
    strokeColor,          // value: UIColor
    strokeWidth,          // value: number
    underlineColor,       // value: UIColor
    strikethroughColor,   // value: UIColor
    paragraphStyle,       // value: NSParagraphStyle
}

```

## UIParagraphStyle

An object that enables changing the values of the subattributes in a paragraph style attribute.

```typescript

/**
 * The distance in points between the bottom of one line fragment and the top of the next.
 */
lineSpacing: number

/**
 * The text alignment of the receiver.
 */
alignment: UITextAlignment

/**
 * The mode that should be used to break lines in the receiver.
 */
lineBreakMode: UILineBreakMode

/**
 * The receiver’s minimum height.
 */
minimumLineHeight: number

/**
 * The receiver’s maximum line height.
 */
maximumLineHeight: number

/**
 * The line height multiple.
 */
lineHeightMultiple: number

```

## Relate

* [Apple Document](https://developer.apple.com/documentation/foundation/nsattributedstring?language=objc)
* [Range](Enums.md)