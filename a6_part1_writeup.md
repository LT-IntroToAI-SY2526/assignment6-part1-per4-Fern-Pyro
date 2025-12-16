# Assignment 6 Part 1 - Writeup

**Name:** _______________  
**Date:** _______________

---

## Part 1: Understanding Your Model

### Question 1: R² Score Interpretation
What does the R² score tell you about your model? What does it mean if R² is close to 1? What if it's close to 0?

I had to look up r2_score, which we imported from sklearn.metrics; R² is the coefficient of determination, which is used to measure the fit of the regression line by comparing the predicted relationship between the dependent and independent variable against real data. The closer R² is to 1, the more accurate the model is and vice versa (the closer R² is to 0, the less correlation is proved by the regression line).



---

### Question 2: Mean Squared Error (MSE)
What does the MSE (Mean Squared Error) mean in plain English? Why do you think we square the errors instead of just taking the average of the errors?

MSE is the average difference between the model’s predictions and true data points/values (the margin of error); squaring the error ensures the MSE is positive.



---

### Question 3: Model Reliability
Would you trust this model to predict a score for a student who studied 10 hours? Why or why not? Consider:
- What's the maximum hours in your dataset?
- What happens when you make predictions outside the range of your training data?

I wouldn’t necessarily trust my model to accurately predict a score for a student who studied 10 hours; the training dataset ranges from 2.3-9.6 hours of studying, which does not encompass any reference points for test scores at 10 hours of studying. When you make perdeictipons outside of this range the model continues on the same trajectory found in the training data set, which may not hold true for a wider range (the pattern doesn’t necessarily continue or stay constant).




---

## Part 2: Data Analysis

### Question 4: Relationship Description
Looking at your scatter plot, describe the relationship between hours studied and test scores. Is it:
- Strong or weak?
- Linear or non-linear?
- Positive or negative?

The relationship between hours studied and test scores is moderate with an upward slope (positive); the relationship isnt perfectly linear, but the best fit line would be.



---

### Question 5: Real-World Limitations
What are some real-world factors that could affect test scores that this model doesn't account for? List at least 3 factors.

**YOUR ANSWER:**
1. Sleep & other basics needs 
2. Time (given for completion)
3. Grading curve and/or scale


---

## Part 3: Code Reflection

### Question 6: Train/Test Split
Why do we split our data into training and testing sets? What would happen if we trained and tested on the same data?

We split our data into training and testing sets in order to compare how our model “learns” versus the real relationship of whatever we are looking at. If we were to train and test on the same data it would appear as though the model has 100% accuracy, but in reality it has just fitted itself to the provided data (“memorizing” the “correct” answers).



---

### Question 7: Most Challenging Part
What was the most challenging part of this assignment for you? How did you overcome it (or what help do you still need)?

The most challenging part of this assignment was determining and eliminating errors. I didn’t run my program incementarly because I was focused on writing the actual code, so it wasn’t until running the finished code that I realized I had errors. I fixed errors mostly one at a time, which was especially inconvenient because the program took a few minutes to run and return an error message. This meant a large chunk of my time was spent waiting for each individual change in order to determine whether I had fixed the problem or not. For some error messages I used Chat GBT to point out discrepancies in my code; these were mostly spelling errors that I was unable to catch because I had been staring at the code for so long. 



---

## Part 4: Extending Your Learning

### Question 8: Future Applications
Describe one real-world problem you could solve with linear regression. What would be your:
- **Feature (X):** Education Level
- **Target (Y):** Wage/Income Level
- **Why this relationship might be linear:** because of an already observed correlation between education and job placement(s).

One real world application of linear regression could be determining the relationship between education level and wage/income level. The “Feature (X)” would be the level of education completed and/or degree earned and the “Target  (Y)” would be the various wage/income levels in dollar amounts. This relationship might be linear because of an already observed correlation between education and job placement(s).



---

## Grading Checklist (for your reference)

Before submitting, make sure you have:
- [ ] Completed all functions in `a6_part1.py`
- [ ] Generated and saved `scatter_plot.png`
- [ ] Generated and saved `predictions_plot.png`
- [ ] Answered all questions in this writeup with thoughtful responses
- [ ] Pushed all files to GitHub (code, plots, and this writeup)

---

## Optional: Extra Credit (+2 points)

If you want to challenge yourself, modify your code to:
1. Try different train/test split ratios (60/40, 70/30, 90/10)
2. Record the R² score for each split
3. Explain below which split ratio worked best and why you think that is

**YOUR ANSWER:**
