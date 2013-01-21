kmeansDilution.R
K. Beck
Jan. 8, 2012

**Objective:** Determine if k-means clustering across the log2 fold change between non-lactating and lactating states can better describe the dilution effect

**Secondary Objective:** Determine best clustering algorithm: PAM or CLARA or mixture







</br>
</br>
**Cow** log 2 fold change pre-puberty to lactation

```
## 2  clusters  0.5372 
## 3  clusters  0.5397 
## 4  clusters  0.4658 
## 5  clusters  0.4916 
## 6  clusters  0.537 
## 7  clusters  0.502 
## 8  clusters  0.5276 
## 9  clusters  0.5191 
## 10  clusters  0.5074 
## Optimal cluster size = 3 
## Mediods
##  -2.336 -0.2987 17.17 
## Overall average silhouette
##  0.4779 
## Aver. silhouette by cluster
##  0.3275 0.7088 0
```

```
## Cluster Info
```

```
##      size max_diss av_diss isolation
## [1,] 6987    8.162  0.6273    4.0056
## [2,] 5025    8.330  0.8935    4.0882
## [3,]   16    8.722  5.6358    0.4993
```

```
## Explore different cluster sizes despite silhouettes
```

```
## k = 6
```

```
## Mediods
##  -1.426 -2.436 -3.728 -0.2534 1.6 17.17 
## Overall average silhouette
##  0.6045 
## Aver. silhouette by cluster
##  0.7436 0.6204 0.6137 0.6845 0.3279 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##         [,1]
## [1,] -1.4258
## [2,] -2.4358
## [3,] -3.7275
## [4,] -0.2534
## [5,]  1.6002
## [6,] 17.1712
## Objective function:	 0.3702
## Clustering vector: 	 int [1:12028] 1 2 2 2 2 1 2 2 2 2 2 2 3 2 1 2 1 1 ...
## Cluster sizes:	    	 3278 3965 1323 2425 1028 9 
## Best sample:
##  [1]    79   363   369   485   675   716   747   835   892  1783  1803
## [12]  2102  2510  3155  3314  3892  4071  4107  4230  4242  4352  5120
## [23]  5134  5288  5456  5460  6064  6378  6391  6507  6526  6931  7022
## [34]  7120  7179  7199  7643  7670  7686  8272  8372  8896  9226 10015
## [45] 10130 10170 10203 10389 10554 10756 10939 11183
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```


</br>
**Human** log 2 fold change colostrum to mature milk

```
## 2  clusters  0.4855 
## 3  clusters  0.4744 
## 4  clusters  0.4983 
## 5  clusters  0.5163 
## 6  clusters  0.5158 
## 7  clusters  0.5031 
## 8  clusters  0.4984 
## 9  clusters  0.5015 
## 10  clusters  0.5066 
## Optimal cluster size = 5 
## Mediods
##  -3.927 -0.7145 -8.056 -1.903 1.367 
## Overall average silhouette
##  0.5792 
## Aver. silhouette by cluster
##  0.6558 0.5439 0.5356 0.7129 0.3433
```

```
## Cluster Info
```

```
##      size max_diss av_diss isolation
## [1,] 2618    2.064  0.6885    1.0199
## [2,] 6099    1.041  0.3957    0.8755
## [3,]  808    5.033  1.2923    1.2188
## [4,] 5212    1.011  0.3885    0.8500
## [5,] 3415    6.728  0.9648    3.2319
```

```
## Explore different cluster sizes despite silhouettes
```

```
## k = 3
```

```
## Mediods
##  -3.617 -1.145 1.423 
## Overall average silhouette
##  0.5259 
## Aver. silhouette by cluster
##  0.4059 0.5804 0.511
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##        [,1]
## [1,] -3.617
## [2,] -1.145
## [3,]  1.423
## Objective function:	 0.8919
## Clustering vector: 	 int [1:18152] 1 2 1 2 2 1 1 2 2 2 2 2 2 2 2 2 1 1 ...
## Cluster sizes:	    	 4715 9559 3878 
## Best sample:
##  [1]   175   253   598  1297  2049  4630  4963  5284  5441  5592  5944
## [12]  6229  6664  7676  8126  8169  8280  8453  9125  9436  9606 10364
## [23] 10433 10568 10734 10784 11967 12221 12745 13000 13197 13447 13743
## [34] 13795 14761 15348 15451 15861 16382 16480 16624 16894 17116 17723
## [45] 17911 18117
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 6
```

```
## Mediods
##  -3.758 -1.052 -6.361 -2.115 0.08959 2.086 
## Overall average silhouette
##  0.5113 
## Aver. silhouette by cluster
##  0.6756 0.5914 0.4198 0.5033 0.4653 0.4239
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##          [,1]
## [1,] -3.75799
## [2,] -1.05212
## [3,] -6.36059
## [4,] -2.11468
## [5,]  0.08959
## [6,]  2.08635
## Objective function:	 0.4722
## Clustering vector: 	 int [1:18152] 1 2 3 2 2 3 4 2 2 2 2 5 4 2 4 2 1 3 ...
## Cluster sizes:	    	 2203 4579 1190 4140 3781 2259 
## Best sample:
##  [1]   175   253   508   515   598  1297  1458  2049  3065  3848  4630
## [12]  4963  5284  5441  5592  5944  6664  7060  7676  8126  8169  8280
## [23]  8453  8860  9125  9436  9606 10433 10568 10734 10784 11826 11837
## [34] 11967 12221 12745 13000 13197 13447 13743 14761 15451 15742 15861
## [45] 16382 16480 17116 17220 17702 17723 17911 18117
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```


</br>
**Cow** absolute change (lactation - pre-pub)

```
## 2  clusters  0.9756 
## 3  clusters  0.9176 
## 4  clusters  0.7042 
## 5  clusters  0.768 
## 6  clusters  0.6019 
## 7  clusters  0.7905 
## 8  clusters  0.5602 
## 9  clusters  0.4831 
## 10  clusters  0.543 
## Optimal cluster size = 2 
## Mediods
##  -14.24 147775 
## Overall average silhouette
##  0.9756 
## Aver. silhouette by cluster
##  0.9983 0
```

```
## Cluster Info
```

```
##       size max_diss  av_diss isolation
## [1,] 12024    61929    111.5     0.419
## [2,]     4   404752 123510.9     2.739
```

```
## Explore different cluster sizes despite silhouettes
```

```
## k = 3
```

```
## Mediods
##  -13.43 -1930 147775 
## Overall average silhouette
##  0.8848 
## Aver. silhouette by cluster
##  0.9353 0.2421 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##           [,1]
## [1,]    -13.43
## [2,]  -1929.82
## [3,] 147775.00
## Objective function:	 120.5
## Clustering vector: 	 int [1:12028] 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 ...
## Cluster sizes:	    	 11764 260 4 
## Best sample:
##  [1]   478   768   820  1116  1285  1581  2501  2527  2562  3155  3900
## [12]  4081  4401  4414  4515  4642  5035  5095  5324  5665  5855  6464
## [23]  6926  7248  7305  7330  7513  7759  7781  8149  8217  8527  8923
## [34]  8979  9295  9783  9785  9906 10167 10570 10586 10644 11092 11701
## [45] 11779 11873
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 7
```

```
## Mediods
##  -8.93 -162.9 -2134 -1304 -3397 147775 -4595 
## Overall average silhouette
##  0.7452 
## Aver. silhouette by cluster
##  0.8706 0.6017 0 0 0 0 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##           [,1]
## [1,]     -8.93
## [2,]   -162.93
## [3,]  -2134.04
## [4,]  -1304.42
## [5,]  -3397.36
## [6,] 147775.00
## [7,]  -4594.81
## Objective function:	 81.97
## Clustering vector: 	 int [1:12028] 1 2 1 2 2 1 2 2 1 2 1 2 1 1 1 2 1 1 ...
## Cluster sizes:	    	 9718 2004 82 139 41 4 40 
## Best sample:
##  [1]    45   519  1026  1249  1692  1750  2724  3049  3081  3155  3306
## [12]  3314  3369  3461  3542  3630  3990  4233  4313  4377  4474  4528
## [23]  4781  4859  4973  5553  5651  5732  5782  6043  6146  6253  6317
## [34]  6374  6384  6736  7258  7495  7726  8021  8107  8675  8821  8868
## [45]  9122  9753  9929  9958 10595 10633 10758 10795 11501 12028
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 8
```

```
## Mediods
##  -37.79 -162.9 -3.498 -1200 -2956 767.3 147775 -4595 
## Overall average silhouette
##  0.6737 
## Aver. silhouette by cluster
##  0.4941 0.7292 0.8391 0 0 0.8466 0 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##            [,1]
## [1,]    -37.787
## [2,]   -162.933
## [3,]     -3.498
## [4,]  -1200.052
## [5,]  -2955.741
## [6,]    767.321
## [7,] 147775.000
## [8,]  -4594.806
## Objective function:	 77.65
## Clustering vector: 	 int [1:12028] 1 2 3 2 2 1 2 2 1 2 1 2 1 1 3 2 1 1 ...
## Cluster sizes:	    	 3006 1847 6820 170 98 43 4 40 
## Best sample:
##  [1]   878   899  1163  1168  1292  1515  1634  1691  1807  1964  2428
## [12]  2455  2471  2602  2900  3023  3057  3155  3157  3309  3314  4039
## [23]  4987  5029  5041  5173  5541  5696  5724  5968  6087  6255  6259
## [34]  6448  6863  6932  7175  7298  7325  7488  7559  7729  9695 10705
## [45] 10814 10911 10920 10928 10969 11165 11508 11737 11812 11933 11947
## [56] 12011
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 12
```

```
## Mediods
##  -33.54 -162.9 -3.935 -490.5 -2467 -1200 -2956 379.3 2091 147775 -1605 -4595 
## Overall average silhouette
##  0.4921 
## Aver. silhouette by cluster
##  0.4332 0.7667 0.508 0.3666 0 0 0.5984 0.4369 0 0 0.9941 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##             [,1]
##  [1,]    -33.540
##  [2,]   -162.933
##  [3,]     -3.935
##  [4,]   -490.538
##  [5,]  -2467.137
##  [6,]  -1200.069
##  [7,]  -2955.741
##  [8,]    379.276
##  [9,]   2091.000
## [10,] 147775.000
## [11,]  -1604.673
## [12,]  -4594.806
## Objective function:	 67.88
## Clustering vector: 	 int [1:12028] 1 2 3 2 2 1 2 2 1 2 1 4 1 1 3 2 1 1 ...
## Cluster sizes:	    	 3219 1676 6559 219 55 72 45 54 19 4 66 40 
## Best sample:
##  [1]    82   251   382   547   743  1493  1528  1875  2492  2557  2866
## [12]  3048  3155  3314  3367  3381  3481  3608  3642  4002  4061  4290
## [23]  4631  4822  5023  5430  5431  5472  5647  5724  5892  6215  6272
## [34]  6296  6378  6448  6480  6514  6733  6747  7166  7183  7270  7493
## [45]  7604  7890  8462  8749  8751  9050  9078  9122  9133  9266  9536
## [56]  9552 10059 10578 10668 10745 10840 11473 11763 11954
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```


</br>
**Human** absolute change (mature - colostrum)

```
## 2  clusters  0.6388 
## 3  clusters  0.374 
## 4  clusters  -0.05918 
## 5  clusters  0.5912 
## 6  clusters  0.6095 
## 7  clusters  0.6127 
## 8  clusters  0.5474 
## 9  clusters  0.609 
## 10  clusters  0.6256 
## 11  clusters  0.3883 
## 12  clusters  0.5275 
## 13  clusters  0.4643 
## 14  clusters  0.6305 
## 15  clusters  0.5027 
## Optimal cluster size = 2 
## Mediods
##  -30.68 -2176 
## Overall average silhouette
##  0.7402 
## Aver. silhouette by cluster
##  0.7651 0.5455
```

```
## Cluster Info
```

```
##       size max_diss av_diss isolation
## [1,] 15831  4722369    1085    2201.7
## [2,]  2321   571375    3806     266.4
```

```
## Explore different cluster sizes despite silhouettes
```

```
## k = 3
```

```
## Mediods
##  -24.41 -2767 4722339 
## Overall average silhouette
##  0.8421 
## Aver. silhouette by cluster
##  0.8793 0.7122 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##            [,1]
## [1,]     -24.41
## [2,]   -2767.32
## [3,] 4722338.57
## Objective function:	 1088
## Clustering vector: 	 int [1:18152] 1 1 1 1 1 1 1 2 1 2 1 1 2 1 2 1 2 2 ...
## Cluster sizes:	    	 16270 1880 2 
## Best sample:
##  [1]   241   414  1289  1290  1437  1560  2029  2184  2346  2443  2529
## [12]  2543  3074  3863  4221  4569  5014  5143  6000  6293  6675  7627
## [23]  7893  7936  8898  8956  9131  9145  9448 10266 11129 11845 12609
## [34] 13615 13701 15662 15711 16145 16407 16540 17083 17450 17666 17813
## [45] 17894 18000
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 7
```

```
## Mediods
##  -4 -958.1 -8845 -132530 681015 -573551 4722339 
## Overall average silhouette
##  0.5694 
## Aver. silhouette by cluster
##  0.7182 0.365 0.2927 0 0 0 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##           [,1]
## [1,]      -4.0
## [2,]    -958.1
## [3,]   -8845.5
## [4,] -132529.9
## [5,]  681015.2
## [6,] -573551.1
## [7,] 4722338.6
## Objective function:	 751.4
## Clustering vector: 	 int [1:18152] 1 1 1 1 1 2 1 2 1 2 1 1 2 1 2 1 2 2 ...
## Cluster sizes:	    	 13970 3680 480 12 6 2 2 
## Best sample:
##  [1]   347   598   933  1106  1167  1216  1432  1511  1981  2285  2739
## [12]  4090  4150  4249  4527  4989  5051  5097  5230  5317  5679  6346
## [23]  6692  7327  7758  9509  9836  9845 10042 10373 10531 11698 11719
## [34] 11951 12977 13112 13123 13596 13780 13791 13819 14090 14568 14962
## [45] 15089 15505 15570 15743 15801 16294 16454 16606 17046 18000
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 10
```

```
## Mediods
##  -4.318 -1009 -6795 8319 -132530 -36762 681015 57171 -573551 4722339 
## Overall average silhouette
##  0.5952 
## Aver. silhouette by cluster
##  0.7687 0.451 0.4147 0.4485 0 0 0 0 0 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##              [,1]
##  [1,]      -4.318
##  [2,]   -1008.635
##  [3,]   -6795.136
##  [4,]    8318.932
##  [5,] -132529.936
##  [6,]  -36761.965
##  [7,]  681015.206
##  [8,]   57170.582
##  [9,] -573551.062
## [10,] 4722338.565
## Objective function:	 616.3
## Clustering vector: 	 int [1:18152] 1 1 1 1 1 2 1 2 1 2 1 1 2 1 2 1 2 3 ...
## Cluster sizes:	    	 13959 3427 567 111 8 57 5 14 2 2 
## Best sample:
##  [1]    86   215   598   933  1170  1639  2139  2965  3008  3239  3970
## [12]  4179  4273  4389  4495  4562  5289  5438  5656  5705  5783  6332
## [23]  6591  6679  6828  7434  7617  9367  9550  9876 10148 10734 11032
## [34] 11123 11455 11760 12195 12219 12522 12738 12907 13549 13780 13811
## [45] 13927 14656 14966 14979 15137 15361 15894 16017 16264 16314 17423
## [56] 17497 17642 17763 17849 18000
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```

```
## k = 14
```

```
## Mediods
##  -11.73 -836.9 -2943 767.7 -7082 -12575 5137 -132530 -16756 -36762 261126 64299 3108792 4722339 
## Overall average silhouette
##  0.6585 
## Aver. silhouette by cluster
##  0.8412 0.6672 0.8619 0.3423 0.4851 0.4268 0 0 0 0 0 0 0 0
```

```
## Call:	 clara(x = data, k = k, samples = 50, pamLike = FALSE) 
## Medoids:
##             [,1]
##  [1,]     -11.73
##  [2,]    -836.94
##  [3,]   -2942.67
##  [4,]     767.66
##  [5,]   -7082.20
##  [6,]  -12575.03
##  [7,]    5137.43
##  [8,] -132529.94
##  [9,]  -16756.13
## [10,]  -36761.96
## [11,]  261125.72
## [12,]   64299.29
## [13,] 3108791.51
## [14,] 4722338.57
## Objective function:	 450.5
## Clustering vector: 	 int [1:18152] 1 1 1 1 1 2 1 2 1 3 2 1 2 1 3 1 3 3 ...
## Cluster sizes:	    	 12587 3073 913 883 283 91 186 10 64 41 7 12 1 1 
## Best sample:
##  [1]   364   366   501   598   763   926   975  1170  1198  1809  2095
## [12]  2184  2884  2924  2948  3833  3984  4429  4473  4678  4774  4919
## [23]  5094  5937  6299  6463  6636  6655  6698  7027  7582  7857  8226
## [34]  9367  9414  9620  9974 10048 10233 10520 10628 10761 10847 11242
## [45] 11923 12192 12222 12568 12673 12740 13036 13112 13289 15645 15699
## [56] 15885 15903 16058 16069 16773 17130 17228 17250 17427 17715 17735
## [67] 17741 18000
## 
## Available components:
##  [1] "sample"     "medoids"    "i.med"      "clustering" "objective" 
##  [6] "clusinfo"   "diss"       "call"       "silinfo"    "data"
```











