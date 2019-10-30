### Date created
October 24th, 2019

### Author
M. Bosquet


### Project Title
Understanding No-shows: A first investigation into factors influencing the
non-attendance of medical appointments in Brazil


### List of Sources
The following sources were used to perform the analysis:

* to separate two variables from one column: <br>
df_clean['Scheduled_Day'] = [d.date() for d in df_clean['ScheduledDay']] <br>
df_clean['Scheduled_Time'] = [d.time() for d in df_clean['ScheduledDay']] <br>
looked
up and adapted from [Stackoverflow](https://stackoverflow.com/questions/35595710/splitting-timestamp-column-into-separate-date-and-time-columns)

* to drop rows with a specific condition: <br>
df.drop(df.index[df['Age'] < 0], inplace = True) <br>
looked up and adapted from [Stackoverflow](https://stackoverflow.com/questions/18172851/deleting-dataframe-row-in-pandas-based-on-column-value)

* color scheme for graphs from [matplotlib documentation](https://matplotlib.org/_images/sphx_glr_named_colors_003.png)

* pie chart extras from [matplotlib documentation](https://matplotlib.org/3.1.1/gallery/pie_and_polar_charts/pie_features.html#sphx-glr-gallery-pie-and-polar-charts-pie-features-py)

* creating histograms from timedelta datatypes: <br>
(datafr['Days_in_Advance']/pd.Timedelta(days=1)).hist(bins=50, label=label, color=color) <br>
 looked up and adapted from [Datasciencebytes](https://www.datasciencebytes.com/bytes/2015/05/16/pandas-timedelta-histograms-unit-conversion-and-overflow-danger/)


### Credits
This project was created as part of a Udacity Nanodegree Course.

The jupyter notebook "Investigate_a_dataset_MBosquet.ipynb" containing the analysis is build from a template provided by [Udacity's Data Analyst Nanodegree]((https://www.udacity.com/course/data-analyst-nanodegree--nd002). The .csv file with the raw data was made available as part of the course and provided by [Kaggle](https://www.kaggle.com/joniarroba/noshowappointments).
