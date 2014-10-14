#PlotALLPCA!

Simple implementation of [Scatterplot Matrix Brushing](http://bl.ocks.org/mbostock/4063663) with some nagivation function

Similiar to R's : 

```
pairs(~C1+C2+C3+C4+C5+C6, df)
```


demo : [Squamous Cell Carcinoma PCA](https://pwbc.garvan.org.au/~xiuque/plotALLPCA/PlotAllThePCA/view.html)



## IMPORTANT!

As the code do not handle negative value very well. You will have to recenter your PCA plot to ensure that all values 
are positive. By convention, PCA plots are zero-centered.


## Usage 

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


To obtain these values from R:

```
x <- matrix(rnorm(1000*6,sd=sd),1000,6)
rownames(x) <- paste("Gene",1:1000)
x<- prcomp(x)
x$rotation ## will contain your data  
```

Note that the colour of the dots will be represented by the sample

 

