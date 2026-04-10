Applies for data queries but doesn´t apply to record creation or changes, including deletions.

When you note a class with SeeAllData=True, annotations for methods with SeeAllData=False will be ignored.
When you note a class with SeeAllData=False, annotations for methods with SeeAllData=True will override the class annotation for this method.