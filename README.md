# DecisionTreeID3

Implement ID3 algorithm for data with all categorical attributes by using panda and numpy (sklearn DecisionTreeClassifier doesn't support categorical attributes).

## Stopping criteria 
* `max_depth`:  the max depth of the tree.
* `min_samples_split`: the minimum number of samples in a split to be considered.
* `min_gain`: minimum gain for splitting. 

## simple test 
```python
df = pd.DataFrame.from_csv('weather.csv')
X = df.iloc[:, :-1]
y = df.iloc[:, -1]
tree = DecisionTreeID3(max_depth = 3, min_samples_split = 2)
tree.fit(X, y)
print(tree.predict(X)) # predict on training data 
```

Result should be: 
```
['no', 'no', 'yes', 'yes', 'yes', 'no', 'yes', 'no', 'yes', 'yes', 'yes', 'yes', 'yes', 'no']
```

It means 100% accuracy on training set. 

Pruning might be added later. 