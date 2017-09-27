# polymorphisms_statistic_analysis
Code for my contribution in a medicine related project/paper with faculty form Kapodistrian University of Athens. 

Analysis was performed in 2x2 contigency tables of populations and relevant alleles for every polymorhism. (Let Matrix ) Fisher Exact test was used for evaluating the statistical significance. https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.fisher_exact.html

All matrices have the following form: 

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{pmatrix}&space;Group&space;1\Join&space;Allele&space;1&space;&&space;Group&space;2\Join&space;Allele&space;1&space;\\&space;Group&space;1\Join&space;Allele&space;2&space;&&space;Group&space;2\Join&space;Allele&space;2&space;\end{pmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{pmatrix}&space;Group&space;1\Join&space;Allele&space;1&space;&&space;Group&space;2\Join&space;Allele&space;1&space;\\&space;Group&space;1\Join&space;Allele&space;2&space;&&space;Group&space;2\Join&space;Allele&space;2&space;\end{pmatrix}" title="\begin{pmatrix} Group 1\Join Allele 1 & Group 2\Join Allele 1 \\ Group 1\Join Allele 2 & Group 2\Join Allele 2 \end{pmatrix}" /></a>

3 main statistical values were extracted: 

P-Value was extracted from fisher exact test.

Odds ratio is exctracted from the expression: 

<a href="https://www.codecogs.com/eqnedit.php?latex=\prod_{i=j}&space;Matrix[i,j]&space;/&space;\prod_{i\neq&space;j}&space;Matrix[i,j]" target="_blank"><img src="https://latex.codecogs.com/gif.latex?OddsRatio=\prod_{i=j}&space;Matrix[i,j]&space;/&space;\prod_{i\neq&space;j}&space;Matrix[i,j]" title="\prod_{i=j} Matrix[i,j] / \prod_{i\neq j} Matrix[i,j]" /></a>

Confidence Interval 95% was computed with the following expression:

<a href="https://www.codecogs.com/eqnedit.php?latex=Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&plus;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&plus;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" title="Upper Limit = exp(ln(OddsRatio)+1.96*\sqrt{\sum \frac{1}{Matrix[i,j]}}))" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=Upper&space;Limit&space;=&space;exp(ln(OddsRatio)&plus;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Lower&space;Limit&space;=&space;exp(ln(OddsRatio)&plus;1.96*\sqrt{\sum&space;\frac{1}{Matrix[i,j]}}))" title="Upper Limit = exp(ln(OddsRatio)-1.96*\sqrt{\sum \frac{1}{Matrix[i,j]}}))" /></a>
