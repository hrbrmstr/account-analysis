README
================
@hrbrmstr
September 14, 2019

Twitter account analysis like [this
one](https://rud.is/dl/hrbrmstr-account-analysis.html).

![](account-analysis-header.png)

A lesser, static version of
[accountanalysis](https://accountanalysis.app).


Can be used in a function call:

```
render_report <-  function(twitterusername, tweetcount = 3000) {

  rmarkdown::render(input = "account-analysis.Rmd",
                    params = list(
                      username = twitterusername,
                      n_tweets_to_retrieve = tweetcount
                      ),
                    output_file = paste0(
                      "AccountAnalysisOf-",
                      twitterusername,
                      ".html"
                    )
  )
  }
```

