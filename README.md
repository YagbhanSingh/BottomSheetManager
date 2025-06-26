# 📦 BottomSheetManager

A fully customizable and reusable **Bottom Sheet Manager** for iOS, built with UIKit in Swift.  
Easily integrate flexible bottom sheet modals across your app with support for **snap points**, **keyboard-safe areas**, **custom backgrounds**, **drag gestures**, and more!

---

## 🚀 Features

- 🪜 **Snap Points Support**: Collapsed, Mid, Full heights
- ✋ **Drag to Expand / Collapse**
- ⌨️ **Keyboard-Safe Padding**
- 🚫 **Tap-to-Dismiss Toggle**
- 🎨 **Blur / Dimmed / Clear Background Options**
- 🔲 **Custom Corner Radius & Shadows**
- 🔁 **Global Singleton Manager for Reuse**
- 🎯 **Lightweight & UIKit Based**

---

## 📸 Preview

![Bottom Sheet Demo](Assets/BottomSheetPreview.gif) <!-- (optional: you can upload a preview gif or image here) -->

---

## 🛠 Installation

### ✅ Manual

Simply drag the `BottomSheetManager.swift` and `BottomSheetViewController.swift` into your project.

---

## 📦 Usage

### Step 1: Present Bottom Sheet

```swift
BottomSheetManager.shared.present(
    contentViewController: YourCustomVC(),
    from: self,
    defaultHeight: 350,
    showDragIndicator: true,
    isDraggableToExpand: true,
    isDraggableToDismiss: true,
    isTapToDismissEnabled: true,
    cornerRadius: 24,
    backgroundStyle: .blurred(style: .systemThinMaterialDark, alpha: 0.6),
    startFullExpanded: false,
    snapPoints: [200, 400, UIScreen.main.bounds.height - 64]
)
````

### Step 2: Dismiss Programmatically

```swift
BottomSheetManager.shared.dismiss()
```

---

## 🧠 Delegate Callbacks (Optional)

Conform to the `BottomSheetControllerDelegate` protocol to receive updates:

```swift
extension YourViewController: BottomSheetControllerDelegate {
    func bottomSheetDidExpand() { ... }
    func bottomSheetDidCollapse() { ... }
    func bottomSheetDidDismiss() { ... }
    func bottomSheetIsDragging(yOffset: CGFloat) { ... }
}
```

---

## 📄 Customization Options

| Parameter               | Description                         | Default Value         |
| ----------------------- | ----------------------------------- | --------------------- |
| `defaultHeight`         | Initial sheet height                | `300`                 |
| `showDragIndicator`     | Show top bar for drag indication    | `true`                |
| `isDraggableToExpand`   | Allow upward drag to expand         | `true`                |
| `isDraggableToDismiss`  | Allow downward drag to dismiss      | `true`                |
| `isTapToDismissEnabled` | Allow tapping background to dismiss | `true`                |
| `cornerRadius`          | Corner radius of sheet              | `16`                  |
| `backgroundStyle`       | Dimmed / blurred / none             | `.dimmed(alpha: 0.6)` |
| `snapPoints`            | Snap points for drag gestures       | `[]` (disabled)       |
| `startFullExpanded`     | Show full screen on start           | `false`               |

---

## 🧪 Example

Want to see it in action? Check out the [Medium article](https://medium.com/@chaudharyyagh/build-a-fully-customizable-bottom-sheet-manager-in-swift-ios-898cb03ea844) for a step-by-step explanation with code breakdown and demo!

---

## 🧾 License

This project is open-sourced under the **MIT License**. Feel free to use, modify, and contribute.

---

## 🙌 Author

Created with ❤️ by [@chaudharyyagh](https://medium.com/@chaudharyyagh)
🔗 Medium: [https://medium.com/@chaudharyyagh](https://medium.com/@chaudharyyagh)
🔗 GitHub: [https://github.com/YagbhanSingh](https://github.com/YagbhanSingh)

---

## ⭐️ Contribute

Found a bug or want to improve the bottom sheet?
Open an issue or submit a pull request — contributions are welcome!

---

Let me know if you'd like a Hindi-translated README or help creating preview images or a sample demo project!
```
