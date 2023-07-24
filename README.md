Introduction
BUSINESS CASE
Microsoft firm wants to venture into Movies industry by creating new movie studio They need: concrete information before venturing into the investment in order to make a viable decision on #Which type of films are doing well in box_office. #Films that are currently doing well in box_office.
Business Understanding
After crosschecking and clear understanding of the available datasets and problem relating to the Microsoft company which,I chose to work with 'tmdb.movies.csv' dataset to perform a concrete analysis, because it has some motive factors which makes a movie to hit and perform well if well analysed after asking the data the right questions examples: *Language. *Release month or date. *Genre. *Popularity *Vote count.

#importing necesssary libraries 
Loading Data In Pandas
#Loading 'tmdb.movies.csv' Data #converting the CSV file format into pandas represents data in tabular format which is more easier to handle and manipilate huge data and assigning it to the object name>>data_movies.
#converting and assigning into pandas
data_movies=pd.read_csv('tmdb.movies.csv')
data_movies            to view loaded data
data_movies.shape      checking data structure​
data_movies.columns    checking data columns
data_movies.head()     checking the first five data
data_movies.tail()     checking the last  five data
data_movies.info        checking data info
data_movies.isnull().sum()   checking  missing values traced
data_movies.describe()      checking statistical summary
data_movies.dtypes      checking data types
data_movies.duplicated().value_counts()   checking duplicate sum
data_movies=data_movies.rename(columns={'Unnamed: 0':'unamed'})  renaming specific columns
data_movies=data_movies.drop(columns=['unamed','original_title']) dropping specified columns
data_movies.columns = [x.title() for x in data_movies.columns]    changing character case using lambda functions
data_movies     loading
French_language=data_movies[data_movies.Original_Language=='Fr']     fetching the specified column
French_language   loading
checking length
plt.pie([English,French],labels=labels,colors=colors,autopct='%.2f')   plotting pie chart
plt.hist(data_movies.Vote_Count, color='g', bins=bins)    plottting histogram
months.plot.box(); plotting box plot
