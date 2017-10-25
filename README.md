# polymorphisms_statistic_analysis
Code for my contribution in a medicine related project/paper in colaboration with National and Kapodistrian University of Athens. 

Statistical analysis of alleles distribution was performed in contingency tables 2x2 (1 degree of freedom) and odd ratios (ORs), as well as the corresponding confidence intervals (95% CI) were calculated. (Let Matrix ) Fisher Exact test was used for evaluating the statistical significance. https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.fisher_exact.html

All matrices have the following form: 

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;Group&space;1\Join&space;Allele&space;1&space;&&space;Group&space;2\Join&space;Allele&space;1&space;\\&space;Group&space;1\Join&space;Allele&space;2&space;&&space;Group&space;2\Join&space;Allele&space;2&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;Group&space;1\Join&space;Allele&space;1&space;&&space;Group&space;2\Join&space;Allele&space;1&space;\\&space;Group&space;1\Join&space;Allele&space;2&space;&&space;Group&space;2\Join&space;Allele&space;2&space;\end{pmatrix}" title="\begin{pmatrix} Group 1\Join Allele 1 & Group 2\Join Allele 1 \\ Group 1\Join Allele 2 & Group 2\Join Allele 2 \end{pmatrix}" /></a>

3 main statistical values were extracted: 

P-Value was extracted from Fisher's exact test.

Odds ratio was exctracted according to the following expression: 

<a href="https://www.codecogs.com/eqnedit.php?latex=\prod_{i=j}&space;Matrix[i,j]&space;/&space;\prod_{i\neq&space;j}&space;Matrix[i,j]" target="_blank"><img src="https://latex.codecogs.com/gif.latex?OddsRatio=\prod_{i=j}&space;Matrix[i,j]&space;/&space;\prod_{i\neq&space;j}&space;Matrix[i,j]" title="\prod_{i=j} Matrix[i,j] / \prod_{i\neq j} Matrix[i,j]" /></a>

Confidence Interval 95% was computed with the following expression:

<a href="https://www.codecogs.com/eqnedit.php?latex=Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&plus;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&plus;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" title="Upper Limit = exp(ln(OddsRatio)+1.96*\sqrt{\sum \frac{1}{Matrix[i,j]}}))" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&space;-&space;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&space;-&space;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" title="Upper Limit = exp(ln(OddsRatio) - 1.96*\sqrt{\sum \frac{1}{Matrix[i,j]}}))" /></a>

Visualization of the similarity between the populations:

[![polys.png](https://s1.postimg.org/3jqql5v92n/polys.png)](https://postimg.org/image/4c3m2wbusr/)
