# DecisionTreeID3

Implement ID3 algorithm for data with all categorical attributes by using panda and numpy (sklearn DecisionTreeClassifier doesn't support categorical attributes).

## Stopping criteria 
* `max_depth`:  the max depth of the tree.
* `min_samples_split`: the minimum number of samples in a split to be considered.
* `min_gain`: minimum gain for splitting. 

## simple test on [weather.csv](weather.csv)

| id | outlook  | temperature | humidity |  wind  | play |
|----|----------|-------------|----------|--------|------|
|  1 | sunny    | hot         | high     | weak   | no   |
|  2 | sunny    | hot         | high     | strong | no   |
|  3 | overcast | hot         | high     | weak   | yes  |
|  4 | rainy    | mild        | high     | weak   | yes  |
|  5 | rainy    | cool        | normal   | weak   | yes  |
|  6 | rainy    | cool        | normal   | strong | no   |
|  7 | overcast | cool        | normal   | strong | yes  |
|  8 | sunny    | mild        | high     | weak   | no   |
|  9 | sunny    | cool        | normal   | weak   | yes  |
| 10 | rainy    | mild        | normal   | weak   | yes  |
| 11 | sunny    | mild        | normal   | strong | yes  |
| 12 | overcast | mild        | high     | strong | yes  |
| 13 | overcast | hot         | normal   | weak   | yes  |
| 14 | rainy    | mild        | high     | strong | no   |

```
python id3.py
```

Result should be: 
```
['no', 'no', 'yes', 'yes', 'yes', 'no', 'yes', 'no', 'yes', 'yes', 'yes', 'yes', 'yes', 'no']
```

It means 100% accuracy on training set. 

Pruning might be added later. 