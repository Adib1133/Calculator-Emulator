# fx-991EX NEON - Scientific Calculator Emulator

A beautiful, feature-rich scientific calculator emulator inspired by the Casio fx-991EX, featuring a neon cyberpunk aesthetic and advanced mathematical capabilities.

## Features

### Basic Operations
- Addition, subtraction, multiplication, division
- Parentheses and order of operations
- Percentage calculations
- Memory functions (MC, MR, M+, M-)

### Scientific Functions
- Trigonometric: sin, cos, tan, arcsin, arccos, arctan
- Hyperbolic: sinh, cosh, tanh (via shift combinations)
- Logarithmic: log (base 10), ln (natural), log(base,value)
- Exponential: e^x, 10^x
- Roots: √ (square root), ³√ (cube root), nth root
- Factorial: x!
- Powers: x², x³, x^y
- Constants: π, e
- Random number generation: Ran#
- Coordinate conversion: Pol(x,y) ↔ Rec(r,θ)
- Absolute value: |x|

### Display Formats
- Decimal (Dec)
- Fraction (Fra)
- Scientific Notation (Sci)
- Degrees-Minutes-Seconds (Dms)

### Angle Modes
- Degrees (Deg)
- Radians (Rad)
- Gradians (Gra)

### Additional Features
- Calculation history (desktop mode)
- Fraction ↔ Decimal conversion
- Engineering notation support
- Answer memory (Ans)
- Variable storage (X)
- Copy to clipboard
- Theme cycling
- Key sound effects
- Responsive design (basic/desktop modes)
- Keyboard shortcuts

## Usage

### Basic Calculations
Enter expressions using the on-screen buttons or your keyboard, then press "=" to evaluate.

### Shift and Alpha Functions
- **Shift** (Shift key): Accesses secondary functions (shown in yellow on keys)
- **Alpha** (A keyst): Accesses alpha functions (shown in red on keys)

### Keyboard Shortcuts
Numbers and basic operators work directly with your keyboard:

```
0-9     : Digits
.       : Decimal point
+ - * / : Basic arithmetic
( )     : Parentheses
^       : Power
%       : Percentage
,       : Comma (for function arguments)
Enter   : Equals (=)
Backspace: Delete
Escape  : All Clear (AC)
← →     : Cursor movement
↑ ↓     : History navigation

Scientific Functions:
s       : sin (Shift+s = arcsin)
c       : cos (Shift+c = arccos)
t       : tan (Shift+t = arctan)
l       : log (Shift+l = 10^x)
n       : ln (Shift+n = e^x)
q       : √ (Shift+q = ³√)
p       : π
e       : e constant
a       : Ans
x       : X variable
!       : Factorial
f       : Cycle display format (Decimal ↔ Fraction ↔ Scientific)
```

### Display Format Cycling
- **SD Button**: Cycle through Decimal → Fraction → Scientific (repeat)
- **Shift+SD**: Toggle Degrees-Minutes-Seconds mode
- **f Key**: Cycle through all formats: Decimal ↔ Fraction ↔ Scientific ↔ DMS

### Angle Mode
- **DRG Button**: Cycle through Degrees → Radians → Gradians

### Themes
Click the theme icon (🎨) in the top-right to cycle through color themes.

### Sound
Click the speaker icon (🔊) to toggle key sounds on/off.

### History (Desktop Mode)
In desktop mode, calculation history appears on the right. Click any entry to reuse it.

## Technical Details

### Mathematical Expressions
The calculator supports:
- Standard arithmetic operations with proper precedence
- Parentheses for grouping
- Function calls: `sin(30)`, `log(100,10)`, etc.
- Constants: `pi`, `e`, `Ans`
- Variables: `X`
- Special functions: `nPr(n,r)`, `nCr(n,r)`, `!`

### Display Formats Explained
- **Decimal**: Standard notation (123.456)
- **Fraction**: Fraction or mixed number format (123 1/2)
- **Scientific**: Always in scientific notation (1.23×10²)
- **DMS**: Degrees-minutes-seconds format (123°45'30.00")

## Implementation Notes

This calculator uses a proper expression parser with:
- Tokenization of input
- Shunting-yard algorithm for infix-to-postfix conversion
- Recursive descent parsing
- Precise floating-point arithmetic with error handling

### Error Handling
- **Syntax ERROR**: Invalid expression
- **Math ERROR**: Mathematical domain error (division by zero, square root of negative, etc.)

## Browser Support
Works in all modern browsers with support for:
- ECMAScript 2015+
- Canvas API (for visual effects)
- Clipboard API (for copy functionality)
- Web Audio API (for sound effects)

## Customization

### Themes
Edit the `THEMES` array in the JavaScript section to modify or add color themes.

### Keyboard Mapping
Modify the `map` object in the `keydown` event listener to change keyboard shortcuts.

## Credits
Inspired by the Casio fx-991EX scientific calculator.
Neon cyberpunk aesthetic design.

---

*Built with HTML5, CSS3, and vanilla JavaScript*