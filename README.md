# UkPropertyTransactionStatistics: Render a statistical bulletin from SDLT transaction data.

The initial goal is to make a web view (available [here](https://dralastaircurrie.github.io/UkPropertyTransactionStatistics/makeTablesAndPlots.html)) of the PDF/Excel release [here](https://www.gov.uk/government/statistics/monthly-property-transactions-completed-in-the-uk-with-value-40000-or-above).

## How it works

We get from input Excel [file](UK_Tables_Aug_2017_monthlies.xlsx) (in future, an R data frame) to hosted web page in three basic steps: 
 * Data are processed and plots and tables are specified with the __R language__, embedded as code chunks in a file which also contains marked up text for headers etc.. This [file](makeTablesAndPlots.Rmd) is in [Rmd](http://rmarkdown.rstudio.com/) format.
  * The R package [__`knitr`__](https://yihui.name/knitr/) renders both the marked-up text and the result of executing the code chunks to a single html [file](makeTablesAndPlots.html).
  * When the html file is pushed to the `gh-pages` branch, __GitHub__ automatically hosts it for us on [github.io](https://dralastaircurrie.github.io/UkPropertyTransactionStatistics/makeTablesAndPlots.html)).
