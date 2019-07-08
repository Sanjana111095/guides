# Missing Values
For a number of reasons, variables will have missing values for certain observations. It is helpful to have the data reflect why these values are missing, particularly for numeric variables. For instance, you may want to know whether someone didn’t answer a question about business revenues because the question was skipped (e.g., they weren’t business owners) or whether it was because they could not remember.

Stata has special codes for missing values. For numeric variables, missing values are considered to be greater in value than all other numbers and themselves have an order. They go like this: . <  .a <  .b <  .c <  .d < ... The .a, .b, etc. are called “extended missing values.” Our standard for which extended missing values correspond with which reasons for missingness can be found here. Note that extended missing values cannot be stored in string variables. 

Work with the field RA to determine what values represent missing values in your data. For instance, sometimes -99 refers to “don’t know”. In that case, you will want to replace all -99 values with .d. It can be helpful to use the recode command to efficiently replace those values.

It might be useful to use cb2html command to detect which missing values were used in the survey or any data entry error. There is also misstable summarize, as well as the user-written mdesc, and missings.

String variables with a missing value are shown as “” (called “blank”). When it is necessary to know why a string variable is missing, select standard strings are used: see [here](Link) for the IPA convention.