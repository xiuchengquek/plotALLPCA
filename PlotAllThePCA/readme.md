#PlotALLPCA!

Simple implementation of [Scatterplot Matrix Brushing](http://bl.ocks.org/mbostock/4063663) with some nagivation function

To use : 
 
 `git clone https://github.com/xiuchengquek/plotALLPCA.git`
 
and place your csv file in the folder.

Since d3.csv require a webserver to be running, you will need to run 

```
 python -m SimpleHTTPServer 8000
```

Alternatively, you can pop the files in the your apacha's public_html folder ( serves a server as well )


By default, it will loads data comprising of PCA loadings from Squamous Cell Carcinoma Project. 
Use the browse function to point to the file of your choice. (remember since it is running as a server, you will have to point the file that is accessible from your server)


The format of you csv file should goes something like this :


```sample,PC1,PC2,PC3,PC4
cancer,1,2,3,3
cancer,2,1,2,3
cancer,4,1,2,4
healthy,1,2,4,5
healthy,1,4,6,7
healthy,4,5,1,2
healthy,5,1,6,7
```

Note that the colour of the dots will be represented by the sample

 

