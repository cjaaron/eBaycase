# eBaycase

---
title: "eBay Experimental Analysis"
author: "Charlotte Aaron & Philip Cooper"
date: "10/29/2017"
output: pdf_document
---

Before we get started on the analysis, here is the code necessary to load the data. We also inputted code to convert the dates from characters to dates in the dataframe for better analysis. 

```{r}
library(readr)
eBayData <- read_csv("~/Library/Mobile Documents/com~apple~CloudDocs/2017 Fall/Business Analytics/ebay case/eBayData.csv")
eBayData$rDate = as.Date(eBayData$date, format="%m/%d/%y")
```

### Header 3  {.css_class} Understanding the Study

```{r}
head(eBayData$rDate)
head(eBayData[eBayData$isTreatmentPeriod == "1",]$rDate)
```

The treatment period began on May 22, 2012, almost two months after the experiment start date, April 1, 2012. Up until the treatment period began, both the treatment group and the control group were viewing the same advertisements for eBay. However, after the treatment period began, the treatment group was no longer shown search ads from eBay. 
