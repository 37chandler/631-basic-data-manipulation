# Assignment 1: Car Listings Data

## Overview
This is the first required programming assignment for SEIS-631: Data Preparation and Analysis. You will work with a dataset of car listings drawn from Craigslist postings in the Midwest. The data contains information about the make, model, year, price, odometer, fuel type, transmission, and other details.  

Your goals are to learn how to inspect, clean, and transform a real dataset using Pandas, and to begin generating simple exploratory statistics and visualizations.  

This assignment is designed to take about 2–3 hours.  

### What does successful work look like? 

Your work should demonstrate that you can independently load, inspect, clean, and explore a real dataset using Pandas. Successful completion means your code runs without errors, your analysis correctly answers the questions posed, and your reflection shows thoughtful engagement with the data cleaning process. See the **Evaluation Criteria** section below for detailed expectations.

---

## Learning Objectives
By the end of this assignment you should be able to:

- Load CSV data into a Pandas DataFrame
- Inspect the structure of a dataset and identify missing values
- Clean and transform variables into more useful forms
- Create new derived variables
- Perform basic filtering, grouping, and aggregation
- Write a brief reflection on the data preparation process and think critically about how preparation decisions affect analysis

---

## Data
The dataset is provided in a compressed zip file on Canvas. Download that data and extract the CSV file to your repository directory. The dataset is named `car_listings.csv`. Remember: we do not want to track large data files in Git. I've set up the `.gitignore` file to exclude CSV files, so you should be safe, but make sure you don't accidentally commit the data file.

The file contains car listings from the following cities:

- Chicago  
- Minneapolis  
- Milwaukee  
- Kansas City  
- St. Louis  
- Madison  
- Grand Rapids  
- Omaha  
- Des Moines  
- Duluth  
- Appleton  
- Fargo  

These data were scraped from Craigslist starting in mid-2023. The dataset contains the following columns:

| Column            | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `url`             | Full URL of the original Craigslist listing                                 |
| `location`        | City where the listing was posted (e.g., `chicago`, `minneapolis`)          |
| `post_id`         | Unique Craigslist identifier for the listing                                |
| `time_posted`     | Timestamp when the listing was posted                                       |
| `name`            | Name of the vehicle from the listing                                        |
| `make`            | Vehicle manufacturer (e.g., Ford, Toyota)                                   |
| `model`           | Vehicle model (e.g., Camry, F-150)                                          |
| `year`            | Vehicle model year                                                          |
| `odometer`        | Reported odometer reading (miles)                                           |
| `title`           | Title status (e.g., clean, salvage, rebuilt)                                |
| `paint`           | Exterior paint color                                                        |
| `drive`           | Drivetrain type (e.g., FWD, RWD, 4WD)                                       |
| `cylinders`       | Engine cylinder count (text as posted, e.g., `4 cylinders`)                 |
| `fuel`            | Fuel type (e.g., gas, diesel, hybrid, electric)                             |
| `type`            | Vehicle body type (e.g., sedan, SUV, truck)                                 |
| `transmission`    | Transmission type (e.g., automatic, manual)                                 |
| `condition`       | Reported condition of the vehicle (e.g., excellent, good, fair)             |
| `vin`             | Vehicle Identification Number (if provided)                                 |
| `price`           | Asking price in U.S. dollars                                                |
| `posting_body_text` | Free-text body of the Craigslist post                                     |
| `title_text`      | Text of the Craigslist listing title                                        |
| `num_images`      | Number of images included in the listing                                    |
| `latitude`        | Latitude coordinate of the listing                                          |
| `longitude`       | Longitude coordinate of the listing                                         |


---

## Instructions
Complete all work in the provided Jupyter Notebook (`Exploring Car Listings.ipynb`). Some of the steps indicated have been taken care of for you to help you get started.

### Part 1: Inspect the Data
Before we can analyze or prepare data, we must understand what it is: its source, structure, scope, and limitations. Use the provided cells to examine dataset shape, data types, summary statistics, and patterns of missing data.


### Part 2: Preparing the Data for Analysis
Before analyzing this data, we need to prepare it by making thoughtful decisions about duplicates, data types, and derived variables.

### Part 3: Handling Missing Data
When we encounter missing values, we have several choices: remove rows, fill (impute) values, or keep them and handle during analysis. Each choice has implications.


### Part 4: Reflection
Write a short reflection wrapping up the assignment. 

---

## Deliverables

When you have completed your work, **follow these steps carefully before submitting**. These will be largely the same on every assignment. 

### 1. Clear All Outputs
Before your final submission, you need to clear all cell outputs to ensure a clean starting state:
- In the notebook menu, select **Kernel → Restart & Clear Output** (or **Kernel → Restart Kernel and Clear All Outputs**)
- This removes all previously generated output and resets the kernel

### 2. Run Everything from Top to Bottom
After clearing outputs, verify that your notebook runs correctly from start to finish:
- Select **Run → Run All Cells** (or **Cell → Run All**)
- Watch the cells execute in order
- Ensure there are no errors
- Check that all outputs appear as expected. In particular, **read** your Markdown cells and ensure they look exactly the way you want, just as you would with an essay assignment. 

**Why is this important?** This process ensures that:
- Your code doesn't depend on cells being run in a specific order that differs from top-to-bottom
- You haven't accidentally deleted a cell that defines a variable used later
- Someone else (including me, when grading) can view your notebook and see the results. If needed, I can also run the notebook and should see the same results. 

### 3. Comment Out Large Outputs (Optional but Recommended)
If any cells print very large DataFrames or long outputs, consider commenting them out or removing the print statements. This keeps your notebook file size manageable and makes it easier to review.

### 4. Commit and Push to GitHub
Once you've verified everything runs correctly:
```bash
git add "Exploring Car Listings.ipynb"
git commit -m "Ready for review"
git push
```
You can also commit by going to the Source Control menu (**View → Source Control** or click on the icon on the left) and using the GUI to do your add-commit-push cycle. Instructions for this are in Module 0 on Canvas. 

**Final checklist before submitting:**
- [ ] Kernel restarted and all outputs cleared
- [ ] All cells run successfully from top to bottom
- [ ] All questions answered in Markdown cells
- [ ] Large debug outputs commented out or removed
- [ ] Changes committed and pushed to GitHub

---

## AI Policy
You may use AI to *ask questions* if you are stuck or need clarification. However, do not use AI code-completion or copy/paste code from AI. The purpose of this assignment is for you to gain fluency with Pandas by writing code yourself.

## Evaluation Criteria

This rubric describes different levels of understanding and skill demonstration. Use it for self-assessment and to understand feedback on your work. Your work will be evaluated more holistically than this rubric implies, but will give you a sense of what I'm looking for at each facet.

### Code Functionality

**Exemplary**: All code executes flawlessly from top to bottom. All required tasks are completed correctly, including data loading, cleaning, transformation, filtering, and calculations. The workflow demonstrates clear understanding of the assignment requirements.

**Proficient**: Code executes with only minor issues that don't prevent completion of major tasks. All required tasks are attempted and most are completed correctly. Any errors are minor and don't indicate fundamental misunderstandings.

**Developing**: Code has some execution errors or several tasks are incomplete. Core functionality is present but needs refinement. Some required transformations or calculations are missing or incorrect.

**Beginning**: Code does not run or has major execution errors. Multiple required tasks are missing or fundamentally incorrect. Demonstrates need for significant additional practice with core concepts.

---

### Data Analysis & Interpretation

**Exemplary**: All analytical questions are answered correctly with clear, data-supported explanations. Demonstrates strong ability to extract insights from data. Calculations are accurate and interpretations show deep engagement with the dataset. Data visualizations support the conclusions directly and adhere to design best practices.

**Proficient**: Most questions are answered correctly. Minor errors in calculation or interpretation may be present but overall understanding is evident. Answers are supported by the data. Data visualizations are less clearly tied to analysis. 

**Developing**: Some questions are answered incorrectly or incompletely. Demonstrates partial understanding but needs improvement in accuracy or depth of analysis. Some unsupported claims or missing evidence. Data visualizations are rudimentary or absent.

**Beginning**: Many questions are unanswered or incorrect. Limited evidence of analytical thinking or data interpretation skills. Needs substantial work on connecting code output to meaningful insights.

---

### Finished Product

**Exemplary**: Code is clean, well-organized, and uses best practices. Variable names are meaningful and consistent. Pandas methods are used efficiently and appropriately. Markdown cells are used for commentary and to divide up the workflow. The notebook is easy to read and follow, with proper markdown formatting and logical flow.

**Proficient**: Code is generally clean and readable. Minor inconsistencies in style or efficiency may exist but don't impede understanding. Notebook organization is logical with adequate formatting.

**Developing**: Code works but has readability issues such as unclear variable names, inconsistent formatting, or inefficient approaches. Notebook organization could be improved. Demonstrates need for more attention to code quality.

**Beginning**: Code is difficult to read or understand. Poor variable naming, lack of organization, or highly inefficient methods. Minimal attention to presentation or professionalism.

---

### Reflection 

In the reflection section, I am looking for thoughtful engagement with the learning process. I seek to learn your challenges, any insights developed during the assignment, and remaining questions. 
