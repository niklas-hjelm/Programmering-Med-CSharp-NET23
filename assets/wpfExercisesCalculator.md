**Exercise 1: Setting up a Basic WPF Window**

**Description:** Begin with the creation of a basic WPF window which will serve as the foundation for our calculator.

**Task:** 
1. Create a new WPF App in Visual Studio.
2. Set the window title to "Simple Calculator" and resize the window to 300x400 pixels.

**Solution:**
1. Open Visual Studio, create a new WPF App project.
2. In the `<Window ...>` tag in `MainWindow.xaml`, set the properties `Title="Simple Calculator"`, `Width="300"`, and `Height="400"`.

---

**Exercise 2: Layout Basic Calculator Buttons**

**Description:** Set up buttons for numbers 0-9 and basic arithmetic operations: +, -, *, /.

**Task:**
1. Create a grid layout with 5 rows and 4 columns.
2. Populate the grid with buttons for numbers 0-9 and arithmetic operations.

**Solution:**
1. In `MainWindow.xaml`, set up a `Grid` with defined rows and columns. Specifically, define 5 `RowDefinitions` and 4 `ColumnDefinitions`.
2. Drag and drop buttons for each number and arithmetic operation into the appropriate grid cells. For example, `Button Content="1"` should be in `Grid.Row="1" Grid.Column="0"`.

---

**Exercise 3: Display Screen**

**Description:** Add a display screen to show input and results.

**Task:**
1. Above the grid of buttons, add a `TextBox` to show calculations.
2. Set its `Name` property to "txtDisplay" and its `FontSize` to "24".

**Solution:**
1. Drag and drop a `TextBox` control at the top of the window.
2. In XAML, set its `Name` property to "txtDisplay" and `FontSize` to "24".

---

**Exercise 4: Implement Number Buttons' Functionality**

**Description:** Make the number buttons functional.

**Task:** 
1. For each number button's click event, append its respective number to `txtDisplay`.

**Solution:**
1. Handle the click event for each number button, e.g., `Button Content="1" Click="NumberButton_Click"`.
2. Inside the event, append the respective number to `txtDisplay.Text` using `txtDisplay.Text += "1";`.

---

**Exercise 5: Implement Operation Buttons' Functionality**

**Description:** Store the chosen arithmetic operation.

**Task:**
1. For each arithmetic button's click event, store the current number and chosen operation.

**Solution:**
1. Declare global variables for the chosen operation and the current number.
2. In the button click events, e.g., `Button Content="+" Click="PlusButton_Click"`, set the current number from `txtDisplay` and store the chosen operation.

---

**Exercise 6: Implement Equals Button**

**Description:** Perform the arithmetic operation when the equals button is pressed.

**Task:** 
1. Add an equals (=) button to the calculator.
2. Implement its functionality to perform the arithmetic operation stored from the previous step and display the result in `txtDisplay`.

**Solution:**
1. Add an "=" button in the grid, e.g., `Button Content="=" Grid.Row="4" Grid.Column="3" Click="EqualsButton_Click"`.
2. Handle its click event to retrieve the current number, perform the arithmetic using the stored operation and number, then display the result in `txtDisplay`.

---

**Exercise 7: Implement Clear Functionality**

**Description:** Add a clear (C) button to reset the calculator.

**Task:** 
1. Add a "C" button to the calculator.
2. Implement its functionality to clear `txtDisplay` and reset any stored operations or numbers.

**Solution:**
1. Add a "C" button in the grid, e.g., `Button Content="C" Grid.Row="0" Grid.Column="3" Click="ClearButton_Click"`.
2. In its click event, reset `txtDisplay.Text` to empty and clear any stored operations or numbers.

---

**Exercise 8: Handle Division by Zero**

**Description:** Ensure the calculator handles division by zero gracefully.

**Task:** 
1. In the equals button functionality, check for division by zero and display an error if attempted.

**Solution:**
1. Before performing division in the `EqualsButton_Click` event, check if the divisor is zero.
2. If zero, display an "Error" message in `txtDisplay`.

---

**Exercise 9: Implement Decimal Point Button**

**Description:** Allow users to input decimal numbers.

**Task:** 
1. Add a decimal point (.) button to the calculator.
2. Implement its functionality to add a decimal point to `txtDisplay` ensuring no more than one decimal point can be added to a number.

**Solution:**
1. Add a "." button in the grid, e.g., `Button Content="." Grid.Row="4" Grid.Column="2" Click="DecimalButton_Click"`.
2. Handle its click event to add a decimal point to `txtDisplay.Text` only if there isn't already one in the current number.

---

**Exercise 10: Styling the Calculator**

**Description:** Improve the visual appearance of the calculator.

**Task:**
1. Adjust the colors, fonts, and margins/paddings to make the calculator more visually appealing.
2. Ensure buttons have a consistent style and that the

 layout is clear and understandable.

**Solution:**
1. In `MainWindow.xaml`, adjust the properties for each control to set colors, fonts, and spacings. For example, set `Button Background="LightGray"`, `Button Margin="5"`, and `Button FontSize="20"`.
2. Ensure a consistent style by using shared styles or explicitly setting properties on each button and control.

---