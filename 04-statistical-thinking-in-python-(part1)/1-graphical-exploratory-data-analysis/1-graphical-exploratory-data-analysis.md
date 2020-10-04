# graphical-exploratory-data-analysis

* Generating a histogram: `plt.hist()` (parameters: `bins`)
* Always label your axes
* Setting Seaborn styling:
    ```
	import seaborn as sns
    sns.set()
    ```
* Bee swarm plot:
    ```
    _ = sns.swarmplot(x='state', y='dem_share', data=df_swing)
    _ = plt.xlabel('state')
    _ = plt.ylabel('percent of vote for Obama')
    plt.show()
    ```
* Empirical cumulative distribution function - ECDF:
    <br>x-value: the quantity you are measuring
    <br>y-value: fraction of data points that have a value smaller than the corresponding x-value
    ```
    x = np.sort(df_swing['dem_share'])
    y = np.arange(1, len(x)+1) / len(x)
    _ = plt.plot(x, y, marker='.', linestyle='none')
    ```