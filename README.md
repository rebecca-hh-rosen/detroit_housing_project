# detroit_housing_project
ML classification project on housing blight in Detroit, MI

See slides for this project at https://bit.ly/2MCz2Ob


Reflections:

Looks like our model does well, but upon reflection of the process, it may be that total_due_parcel is highly correlated with the target varialbe, total tickets. As such, the next iteration of the project will be applying the methods that time didn't allow along the way.

This will include:

- Up and Down Sampling
- Various other modeling techniques such as grid search
- Look at a baseline model and null accuracy
- Deploy grid (and possibly) random search to find optimal tree depth
- Observe evaluation metrics (including confusion matrix) for each class
- Try a more thorough EDA distribution of each feature again target and improve upon current visualizations
- Scale and normalize each variable more thoroughly
- Eventually try a multi-class target, 0 tickets, 1-7 tickets and 8+ tickets
