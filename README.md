# iowa-climbing-analysis

## Overview and Problem Statement
This project uses data sourced from Mountain Project to explore the available rock climbing routes in Iowa, their types, subtypes, wall locations, safety ratings, and average climber reviews. Following preliminary data analysis, I examined...

1. Question
2. Question
3. Question

## Cleaning Process

### Blanks, Duplicates, Spaces, Formatting
- **Filter tool** for blank cells and removed rows with missing data.
- **Conditional formatting** to highlight and remove duplicates.
- **TRIM() function** to find and remove extra spaces in cells.
- **Spellcheck**

### Refining Process

**Text to Column** to separate...
- Location - Wall Name, Geographic Location, and Nearest City. Added nearest city as necessary. 
- Type - Route Type (Sport, Trad, or Toprope), Top Rope (TR) Access, and Aid (Y/N).
- Rating - Yosemite Decimal System, V-scale, and Safety Ratings. (If more than one rating was listed, the higher difficulty or higher risk rating was kept).

**Format as number** for Avg Rating to one decimal point.

Removed rows with routes under 20ft. 
Removed Bouldering routes not listed concurrently with Sport, TR, or Trad. 
~~Moved Boulder routes and ratings to a separate sheet.~~ Lost upon program crash (along with data cleaning comments). 


