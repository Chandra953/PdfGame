# PdfGame

## Overview
This project demonstrates how to abuse PDF field objects to render a monochrome grid and create an interactive experience where users can input values into text fields. The solution leverages the rendering capabilities of PDFium (used in Chromium-based browsers) and PDF.js (used in Firefox). 

The generated PDF will:
1. Display a monochrome grid.
2. Allow users to enter values using text fields.

This setup has been tested on PDFium and PDF.js but might require modifications for compatibility with Adobe Acrobat.

---

## Features
- **Monochrome Grid Rendering:** Displays a grid made entirely of PDF field objects.
- **Interactive Input Fields:** Allows users to enter values into each grid cell using keyboard input.
- **Lightweight:** Does not require external libraries or scripts outside the PDF viewers.

---

## Prerequisites
- Python 3.x
- Libraries: `reportlab`, `PyPDF2` (Install using `pip install reportlab PyPDF2`)

---

## How It Works
The script generates a PDF with a grid by:
1. Using the **ReportLab** library to create the grid layout.
2. Adding interactive text fields to each grid cell with **PyPDF2**.
3. Saving the interactive PDF for use in compatible viewers.

---

## Installation
1. Clone or download this repository.
2. Install the required libraries by running:
   ```bash
   pip install reportlab PyPDF2
   ```

---

## Usage
1. Open the provided Python script (`interactive_grid_generator.py`).
2. Customize the grid dimensions and file paths as needed (refer to the "Customization" section below).
3. Run the script:
   ```bash
   python interactive_grid_generator.py
   ```
4. Open the generated PDF (`interactive_grid.pdf`) in a compatible viewer like Chrome or Firefox.

---

## Customization
### Modify Grid Dimensions
Adjust the number of rows and columns in the grid by changing the following variables in the script:
```python
rows = 10  # Number of rows in the grid
cols = 10  # Number of columns in the grid
```

### Adjust Cell Size
Modify the size of each grid cell:
```python
cell_width = 40  # Width of each cell (in points)
cell_height = 40  # Height of each cell (in points)
```

### File Paths
Change the output PDF file name if required:
```python
output_file = "interactive_grid.pdf"
```

---

## Testing
Open the `interactive_grid.pdf` in:
1. **Chrome (PDFium):** Interactive fields and grid rendering should work seamlessly.
2. **Firefox (PDF.js):** Similar behavior as Chrome.
3. **Adobe Acrobat (Optional):** May require adjustments for full compatibility.

---

## Limitations
- Tested only on PDFium and PDF.js rendering engines.
- May require additional debugging for use in Adobe Acrobat or other PDF viewers.
- The grid is monochrome and designed for simple applications.

---

## Future Enhancements
- Add support for color-coded grids.
- Include validation logic for user inputs.
- Export entered data to an external file or database.

---

## License
This project is open-source and free to use under the MIT License.

---

## Troubleshooting
### "Cannot open this file" Error
Ensure that you are opening the PDF in a compatible viewer such as Chrome or Firefox.

### Text Fields Not Interactive
Verify the script ran successfully and generated the fields. Recheck the output file path.

---

Feel free to contribute or report issues to improve this project!
