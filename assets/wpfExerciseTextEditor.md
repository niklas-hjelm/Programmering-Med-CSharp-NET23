## Exercise: Simple Text Editor

**Exercise 1: Setting up a Basic WPF Window**

**Description:** Start with the creation of a basic WPF window which will serve as the foundation for our text editor.

**Task:** 
1. Create a new WPF App in Visual Studio.
2. Set the window title to "Simple Text Editor" and resize the window to 600x400 pixels.
---

**Exercise 2: Add a RichTextBox Control**

**Description:** The RichTextBox control allows users to enter and format text.

**Task:**
1. Drag and drop a RichTextBox control onto the window.
2. Set its `Name` property to "txtEditor".
3. Resize and position it to occupy most of the window space, leaving some space at the top for toolbar buttons.

---

**Exercise 3: Add Basic Editing Buttons**

**Description:** Introduce basic editing functionalities: Save, Load, and Clear.

**Task:**
1. Above the RichTextBox, add three buttons: Save, Load, and Clear.
2. Set their `Name` properties respectively: btnSave, btnLoad, btnClear.

---

**Exercise 4: Implement Save Functionality**

**Description:** Enable the user to save the content of the RichTextBox to a text file.

**Task:** 
1. In the button click event for btnSave, implement functionality to save the contents of txtEditor to a file using the SaveFileDialog.

---

**Exercise 5: Implement Load Functionality**

**Description:** Enable loading text from an external file into the RichTextBox.

**Task:**
1. In the btnLoad click event, implement functionality to load a text file's content into txtEditor using the OpenFileDialog.

---

**Exercise 6: Implement Clear Functionality**

**Description:** Allow users to clear the content of the RichTextBox.

**Task:** 
1. For the btnClear click event, clear the content of the txtEditor.

---

**Exercise 7: Add Font Size ComboBox**

**Description:** Introduce a ComboBox to change the font size of the selected text in the RichTextBox.

**Task:** 
1. Add a ComboBox next to the editing buttons.
2. Populate the ComboBox with font sizes: 8, 10, 12, 14, 16, 18, 20.
3. Implement functionality to change the font size of the selected text in the txtEditor upon selecting a size from the ComboBox.

---

**Exercise 8: Implement Text Formatting**

**Description:** Allow users to apply basic text formatting - Bold, Italic, and Underline.

**Task:** 
1. Add three buttons: Bold, Italic, and Underline next to the ComboBox.
2. Implement functionality to apply the respective text formatting to the selected text in txtEditor when each button is clicked.

---

**Exercise 9: Add a StatusBar**

**Description:** Display the number of characters in the txtEditor.

**Task:** 
1. Add a StatusBar at the bottom of the window.
2. Display the character count of txtEditor in the StatusBar.
3. Update the character count every time the text changes in txtEditor.

---

**Exercise 10: Implement Theme Change**

**Description:** Allow users to switch between Light and Dark themes for the text editor.

**Task:**
1. Add a ComboBox at the top with two items: Light and Dark.
2. Implement functionality to switch between the light and dark themes for the entire window based on the selected item in the ComboBox.


## Solution:

**Exercise 1: Setting up a Basic WPF Window**

1. **Open Visual Studio** and click on `Create a new project`.
2. Search for `WPF App` and select it.
3. Name the project as you wish and select a location to save it, then click on `Create`.
4. Once the project is created, go to the `MainWindow.xaml` file.
5. In the `<Window ...>` tag, set the properties `Title="Simple Text Editor"` and `Width="600"` and `Height="400"`.

---

**Exercise 2: Add a RichTextBox Control**

1. Go to the `Toolbox` (usually on the left side).
2. Find `RichTextBox` and drag & drop it onto the MainWindow design view.
3. Set its `Name` property in XAML as `Name="txtEditor"`.
4. Adjust its margins or set height and width properties to occupy most of the window, leaving space at the top.

---

**Exercise 3: Add Basic Editing Buttons**

1. From the `Toolbox`, drag & drop three `Button` controls above the `RichTextBox`.
2. For each button, set their `Name` properties in the XAML as: `btnSave`, `btnLoad`, and `btnClear`.
3. Also, set their `Content` property respectively: "Save", "Load", and "Clear".

---

**Exercise 4: Implement Save Functionality**

1. Double click the `Save` button in the designer to create a click event.
2. Inside the generated `btnSave_Click` method, instantiate a `SaveFileDialog`.
3. Set a filter to save files as `.txt`.
4. If the user chooses a file path, use `File.WriteAllText(path, txtEditor.Text)` to save the file.

---

**Exercise 5: Implement Load Functionality**

1. Double click the `Load` button to create a click event.
2. Inside `btnLoad_Click`, instantiate an `OpenFileDialog`.
3. Set a filter to open `.txt` files.
4. If the user chooses a file, use `File.ReadAllText(path)` to read the file and set the result to `txtEditor.Text`.

---

**Exercise 6: Implement Clear Functionality**

1. Double click the `Clear` button to create a click event.
2. In the `btnClear_Click` method, set `txtEditor.Text = string.Empty`.

---

**Exercise 7: Add Font Size ComboBox**

1. From the `Toolbox`, drag & drop a `ComboBox` next to the buttons.
2. In XAML, populate it with items ranging from 8 to 20 for font sizes.
3. Handle the ComboBox's `SelectionChanged` event. Inside, change the font size of the selected text of `txtEditor`.

---

**Exercise 8: Implement Text Formatting**

1. Add three more buttons named `btnBold`, `btnItalic`, and `btnUnderline`.
2. Set their text/content respectively.
3. For each button's click event, change the style of the selected text in `txtEditor` based on the button pressed.

---

**Exercise 9: Add a StatusBar**

1. Drag & drop a `StatusBar` to the bottom of the MainWindow from the `Toolbox`.
2. Add a `TextBlock` inside the `StatusBar` and name it `statusCharacterCount`.
3. Handle `txtEditor`'s `TextChanged` event and inside, update the `TextBlock` with the character count.

---

**Exercise 10: Implement Theme Change**

1. Add a `ComboBox` at the top and populate it with two items: "Light" and "Dark".
2. Handle its `SelectionChanged` event. Based on the selected item, adjust the `Background` and `Foreground` properties of the MainWindow and its controls to achieve the desired theme.
