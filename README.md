# iowa-climbing-analysis

## **Goal**
Examined
1. What are the average quality and difficulty ratings of routes by location? What are the average quality and difficulty ratings by type of route (sport, trad, TR)?
2. Where is the best location for beginner, intermediate, and advanced climbers to find the most amount of high quality routes? At which climbing walls are they located?

## **Description**
This project uses data sourced from Mountain Project to explore the available rock climbing routes in Iowa, their types, subtypes, wall locations, safety ratings, and average climber reviews. The analysis aimed to extract relevant insights on climb quality, grade, and location. Key tasks included data extraction, data cleaning and refining, exploratory data analysis, and data visualization. 

# Cleaning and Refining
Note - I had initially kept track of data cleaning and changes using comments. These were deleted when program crashed, along with sheet containing extracted bouldering data. Lesson learned! In the future I will be keeping a separate copy of cleaning/refinding notes.

## Blanks, Duplicates, Spaces, Formatting
- **Filtered** for blank cells and removed rows with missing data.
- Used **Conditional formatting** to highlight and remove duplicates.
- Used **TRIM() function** to find and remove extra spaces in cells.
- Used **Format as number** for Avg Rating to one decimal point.
- Reviewed for consistent naming conventions (e.g. 5.10a, not 5.10A).
- Used **Text to Column** to separate...
-    Location - Wall Name, Geographic Location, and Nearest City. Added nearest city as necessary. 
-    Type - Route Type (Sport, Trad, or Toprope), Top Rope (TR) Access, and Aid (Y/N).
-    Rating - Yosemite Decimal System, V-scale, and Safety Ratings. (If more than one rating was listed, the higher difficulty or higher risk rating was kept).
- Used **VLOOKUP** to convert grades from the Yosemite Decimal System to the [IRCRA recommended universal scale](https://www.ircra.rocks/single-post/2016/09/12/reporting-grades-in-climbing-research) (see image below). This eliminated issues with analyzing grades with subdivisions (i.e. 5.10c or 5.8+)

## Relevance and Accuracy
- Cross-referenced state park and climbing databases.
- Added nearest city to missing fields. 
- Removed rows with routes under 20ft. 
- Removed Bouldering routes not listed concurrently with Sport, TR, or Trad.
-    Moved bouldering routes and ratings to separate sheet (lost during program crash).

![image](https://github.com/user-attachments/assets/2fcf326c-2ae1-407e-b16c-4a38eecd3c9b)

# Exploratory Data Analysis (EDA)
Total Routes	138
Avg Star Rating	2.8
Avg Difficulty Rating	11
Max Difficulty Rating	17
Min Difficulty Rating	7
Median Difficulty Rating	10
Mode Difficulty Rating	10
Max Star Rating	4
Min Star Rating	-1
Median Star Rating	2.8
Mode Star Rating	3
![image](https://github.com/user-attachments/assets/0146cb02-6fda-4416-8d65-0af41a56ed79)


