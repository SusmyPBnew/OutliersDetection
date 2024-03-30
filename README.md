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
  <li>Second we using <b>Percentile method</b> to find the outliers,for that we set upper limit as .95 & lower limit as .05.Then we > upper_limit and < lower_limit as outliers containing data.Then we < upper_limit and > lower_limit  as no outliers containing data.Then take a length difference b/n two datasets is the outlier .ie,<b>1211</b>.We draw a box plot & distplot against this.</li>
    <li>Third we using <b>IQR method</b> to find the outliers,for that we find Q1 & Q3.Then find IQR as Q3-Q1.Then find lower_whisker(Q1-1.5*IQR) & upper_whisker(Q1+1.5*IQR).Finding outliers as <lower_whisker & >upper_whisker.Finding no outliers as >lower_whisker & <upper_whisker.Then take a length difference b/n two datasets is the outlier .ie,<b>1142</b>.We draw a box plot & distplot against this. </li>
  <li>Fourth we using <b>Normal distribution</b> to find the outliers,for that we find the mean & standardDeviation of price_per_sqft.So here we find -3sigma & +3sigma.Finding outliers as <-3sigma & >+3sigma.Finding no outliers as >-3sigma & <+3sigma.Then take a length difference b/n two datasets is the outlier .ie,<b>5</b>.We draw a box plot & distplot against this.</li>
 <li>Fifth we using <b>Zscore method</b> to find the outliers,for that we find the mean & standardDeviation of price_per_sqft.So here we find -3sigma & +3sigma.Finding outliers as <-3sigma & >+3sigma.Finding no outliers as >-3sigma & <+3sigma.Then take a length difference b/n two datasets is the outlier .ie,<b>5</b>.We draw a box plot & distplot against this.Zscore method is same as like normal distribution.</li>
</ol>

<p>Finally we finding correlation between all numerical columns using corr() function.For the image representation we are using heatmap & scatterplot here.We find some conclusions are given below,</p>
<ul>
<li>Firstly,  there is a weak negative correlation <b>"-0.01"</b> between total_Sqft and price_per_sqft,there's almost <u>no linear relationship</u> between these two variables.</li>

<li>However, Total Sqft shows <u>moderate positive correlations</u> with other key variables such as bhk <b>"0.34"</b>, price <b>"0.57"</b>, and bath <b>"0.39"</b>, indicating that as the total square feet increases, the number of bedrooms, the property price, and the number of bathrooms tend to increase as well, though not in a perfectly linear manner.</li>

<li>Bath exhibits a <u>strong positive correlation</u> <b>"0.90"</b> with BHK, suggesting a strong linear relationship between the number of bathrooms and the number of bedrooms. Additionally, Bath also demonstrates <u>moderate positive correlations</u> with price <b>"0.45"</b> and total_sqft <b>"0.39"</b>, indicating that properties with more bathrooms tend to command higher prices and have larger square feet.</li>

<li>Price also exhibits <u>moderate positive correlations</u> with bhk <b>"0.39"</b> and total_sqft <b>"0.57"</b>, indicating that both the number of bedrooms and the total square footage have a positive impact on property prices, though again, not in a perfectly linear manner.</li>

<li>Overall, these correlation coefficients provide valuable insights into how different factors are interrelated within our dataset, aiding in better understanding and potentially predicting property prices based on their characteristics.</li>
</ul>



