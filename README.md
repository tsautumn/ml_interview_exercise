# audette_ml_exercise
ML interview exercise for Audette

### Files
#### For the exercise
- Exercise.ipynb - a template that appropriately loads the data and the questions
- dataset.csv - training/test data
- questions.csv - three rows for prediction and discussion

### For Audette
- Generate.ipynb - Poorly documented notebook to create training and question data
- Building....xlsx - your raw excel, needed by Generate.ipynb
- Demo.ipynb - an example solution with LGBM
- requirements.txt - environment *I* used for Generate.ipynb.
- poetry/pyproject/.pythhon-version - if you have to ask, you can ignore them.


### Assignment
1. Create and test a very basic-but-functional ensemble tree classifier (eg, LightGBM) using dataset.csv.  
    - The label column is "system_type".  
    - Exercise.ipynb is provided to save you some time.  
    - Don't overthink this -- we'll be evaluating you on step 3.  Accuracy > 80% gets you a score of 100% on step 1.

2. Apply your model to the three rows in questions.csv.

3. Do a short writeup about your model.  Keep it down to about 300 words, point form is fine.  Speak to:
    - Key assumptions, concerns, and limitations
    - How would you verify that you haven't overfitted?
    - If you were going to do some data cleaning, which features would you look at first, and why?
    - Next steps in making the model more robust?

4. Imagine you're asked to make a very expensive recommendation based on the model's prediction.  How do you feel for each of row 1, 2, and 3 in questions.csv?

### Rubric
- I'll help you evaluate their discussion.  Some of it might make great interview discussion-fodder.

- Did they acknowledge leaving defaults in the classifier?   

- One important default is that TRAIN_FRAC in the template notebook is at .5.  That's a weird choice, so if they leave it without discussion, that's a flag.  No matter what they choose, ask them why they chose it in the interview and take notes for me.

- Did they discuss hyperparameter tuning?

- Regarding their predictions:
	- Row 1 should be very confident
	- Row 2 should not be confident
	- Row 3 is the trick question.  Very unlikely they'll catch it in the exercise, there's no time to do a proper data evaluation.  But you could lead them to it in the interview.  EG: "You didn't really have time for data analysis, but row 3 has two values higher than anything in the training data.  They're both in the top 5 most important features.  How much does that shake your confidence in the prediction?"