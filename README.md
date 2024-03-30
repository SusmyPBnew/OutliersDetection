# OutliersDetection

## Steps Following For Outliers Detection

<ol>
<li>First we check the given csv have any null values and duplicate values in it.For that we use a command that isnull().sum() & duplicated().sum() respectively.</li>
<li>After that we find the outliers in our data using some methods are listed below,</li>
<ul>
  <li>Mean Function</li>
<li>Percentile method</li>
<li>IQR(Inter quartile range method)</li>
<li>Normal distribution</li>
<li>Zscore method</li>
</ul>
  <li>First we using <b>mean function</b> to find the outliers,for that we find the mean & median of price_per_sqft.So here we can see that a difference in it.So outliers in it.</li>
  <li>We use quantile() method to find percentiles .We set some quantiles as 0.05,0.1,0.25,0.5,0.75,0.90,0.92,0.94,0.96,0.98,0.99.From this output a significant variation between 98 & 99 percentile.So outliers exists in it.Here >.95 are outliers data & <.95 are non-outliers data.Then substract its length.We get the outlier as <b>609</b> & we have achieved a bell shaped curve in the distplot</li>
  <li>First we using <b>Percentile method</b> to find the outliers,for that we set upper limit as .95 & lower limit as .05.Then we > upper_limit and < lower_limit as outliers containing data.Then we < upper_limit and > lower_limit  as no outliers containing data.Then take a length difference b/n two lists is the outlier .ie,<b>1211</b>.We draw a box plot & distplot against this.</li>
  



    
</ol>






