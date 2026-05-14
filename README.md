# ✅ Input Validation Library for C++

## Overview 🎯

The **clsInputValidate** library is a powerful C++ class designed to simplify user input validation and safe reading operations. It provides comprehensive functionality for validating and reading various numeric data types and dates, ensuring data integrity and proper error handling in your applications.

## Features ✨

- **Numeric Range Validation**: Check if numbers fall within specified ranges
  - Support for multiple data types (short, int, float, double)
  - Overloaded methods for flexible range checking
  - Easy-to-use comparison functions

- **Number Input Reading** 📝
  - Read integers, short integers, floats, and doubles safely
  - Automatic error handling for invalid input
  - Custom error messages for user feedback
  - Buffer clearing on invalid input

- **Range-Based Input Reading** 🔢
  - Read numbers with automatic range validation
  - Prompt users until valid input is received
  - Support for all numeric types (short, int, float, double)
  - Customizable error messages for out-of-range values

- **Date Validation** 📅
  - Validate dates using the clsDate library
  - Check if dates fall within specified date ranges
  - Support for date comparison operations
  - Integration with clsDate library for powerful date handling

- **String Input Reading** 📄
  - Read entire lines of text safely
  - Support for strings with spaces
  - Automatic whitespace handling

## Installation 📦

1. **Download the clsInputValidate library** from this repository
2. **Download and include the required dependencies**:
   - **clsString library** from your GitHub account and place it in the same directory
   - **clsDate library** from your GitHub account and place it in the same directory
3. Include the header file in your project:

```cpp
#include "clsInputValidate.h"
```

> **Important Note**: The `clsInputValidate` library depends on both `clsString` and `clsDate` libraries for its full functionality. Make sure both header files are in the same directory as `clsInputValidate.h` for the library to work without issues.

## Usage Example 💡

```cpp
#include <iostream>
#include "clsInputValidate.h"

using namespace std;

int main() {
    // Read an integer with error handling
    int Age = clsInputValidate::ReadIntNumber("Please enter your age: ");
    
    // Read an integer within a specific range
    int Score = clsInputValidate::ReadIntNumberBetween(0, 100, 
        "Score must be between 0 and 100, try again:\n");
    
    // Read a double number
    double Salary = clsInputValidate::ReadDblNumber("Enter salary: ");
    
    // Read a double within a range
    double Height = clsInputValidate::ReadDblNumberBetween(100, 300, 
        "Height must be between 100 and 300 cm:\n");
    
    // Validate if a number is within range
    if (clsInputValidate::IsNumberBetween(Score, 0, 100)) {
        cout << "Valid score!" << endl;
    }
    
    // Read a string
    string UserName = clsInputValidate::ReadString();
    
    // Validate a date
    clsDate MyDate(15, 6, 2025);
    if (clsInputValidate::IsValideDate(MyDate)) {
        cout << "Valid date!" << endl;
    }
    
    // Check if a date is within a range
    clsDate StartDate(1, 1, 2025);
    clsDate EndDate(31, 12, 2025);
    if (clsInputValidate::IsDateBetween(MyDate, StartDate, EndDate)) {
        cout << "Date is within the specified range!" << endl;
    }
    
    return 0;
}
```

## Class Structure 🏗️

### Main Methods:

| Method | Description |
|--------|-------------|
| `IsNumberBetween(Number, From, To)` | Validates if a number is within range (supports short, int, float, double) |
| `IsDateBetween(Date, From, To)` | Validates if a date falls within a date range |
| `ReadIntNumber(ErrorMessage)` | Reads an integer with error handling |
| `ReadIntNumberBetween(From, To, ErrorMessage)` | Reads an integer within a specified range |
| `ReadShortNumber(ErrorMessage)` | Reads a short integer with error handling |
| `ReadShortNumberBetween(From, To, ErrorMessage)` | Reads a short integer within a range |
| `ReadFloatNumber(ErrorMessage)` | Reads a float number with error handling |
| `ReadFloatNumber(From, To, ErrorMessage)` | Reads a float within a range |
| `ReadDblNumber(ErrorMessage)` | Reads a double number with error handling |
| `ReadDblNumberBetween(From, To, ErrorMessage)` | Reads a double within a range |
| `IsValideDate(Date)` | Validates a date object |
| `ReadString()` | Reads a complete string line including spaces |

## Requirements 📋

- C++ compiler (C++11 or later)
- **clsString** library (must be downloaded separately and placed in the same directory)
- Standard C++ libraries (`<iostream>`, `<string>`, `<ctime>`)

## Dependencies 🔗

This library requires:
- **clsString Library**: A companion string manipulation library that handles string splitting and parsing operations

Both libraries must be kept in the same directory for proper functionality.

## Future Updates 🚀

This library is actively maintained with planned enhancements:
- Additional date formatting options
- More sophisticated date arithmetic operations
- Localization support for different date formats
- Performance optimizations
- Enhanced error handling

We are committed to continuously improving this library based on community feedback.

## Author 👨‍💻

**Ali Talal Ibrahem**

**Date**: May 14, 2026

---

*This library is provided as-is for educational and practical use in C++ projects involving date operations.*