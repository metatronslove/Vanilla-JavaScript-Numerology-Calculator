# Vanilla JavaScript Numerology Calculator

A pure JavaScript implementation of the "Le Film de Ta Vie" numerology calculator originally created in jQuery (2018 version).

## Features

- **Multiple Calculation Bases**:
  - Logarithmic (A=1, B=2...Z=26)
  - Base 3, 6, 9, 36, and 100 systems
  - Inverse calculations for each base

- **Special Calculations**:
  - "Nostra" mode (removes vowels before calculation)
  - Difference calculations between normal and inverse values

- **Number Processing**:
  - Automatic conversion of numbers to French words
  - Supports numbers up to millions

- **Visual Indicators**:
  - Highlights "warning numbers" (111, 222, 333, etc.)
  - Color-codes matching normal/inverse values

## Usage

1. Enter any text (words or numbers) in the input field
2. The calculator will automatically:
   - Convert numbers to French words
   - Calculate values for all bases
   - Display normal and inverse calculations
   - Show processed text with and without vowels

## Technical Details

### Calculation Methods

- **Normal Values**: Standard alphabetical position (A=1 to Z=26)
- **Inverse Values**: Reverse alphabetical position (A=26 to Z=1)
- **Base Systems**:
  - Base 3: Normal value × 3
  - Base 6: Normal value × 6
  - Base 9: Normal value × 9
  - Base 36: Special extended mapping (A=36 to Z=61)
  - Base 100: Extended mapping (A=100 to Z=125)

### Special Features

- **Number Conversion**: Uses French word equivalents (e.g., "123" → "cent vingt-trois")
- **Warning Numbers**: Highlights significant numbers in red:
  ```js
  ["111","222","333","303","444","555","666","777",
   "270","337","367","370","371","810","1110",
   "1998","3330","6660"]
  ```
- **Matching Values**: Highlights in gold when normal and inverse values match

### Code Structure

- **Pure Vanilla JavaScript** (no jQuery or dependencies)
- **Modular Functions**:
  - `numberToFrenchWords()`: Converts numbers to French words
  - `convertNumbersToWords()`: Processes text to replace numbers
  - `calculateValues()`: Core calculation engine
  - `processInput()`: Main processing function

## Comparison with Original (2018 jQuery Version)

| Feature               | This Version | Original (2018) |
|-----------------------|--------------|-----------------|
| Framework             | Vanilla JS   | jQuery          |
| Number Conversion     | Yes          | Yes             |
| Warning Highlights    | Yes          | Yes             |
| Matching Highlights   | Yes          | Yes             |
| DOM Manipulation      | Native       | jQuery          |
| Code Size             | ~30KB        | ~40KB           |
| Dependencies         | None         | jQuery          |

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). No IE support.

## Donation Information

The calculator includes optional donation links to support the developer. These are the same as in the original version.

## License

Open-source. Originally created by [Le Film de Ta Vie](https://web.archive.org/web/20181206102313/https%3A%2F%2Flefilmdetavie.nexgate.ch%2F).

---

**Note**: This is a faithful recreation of the original calculator's functionality using modern vanilla JavaScript, maintaining all the original features while improving code organization and performance.
```