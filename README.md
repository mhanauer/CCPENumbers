---
title: "ConnectionsStudy"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Load stats packages
```{r}
library(lubridate)
```
CCPE Numbers per year
```{r}
ccpe_numbers$Baseline.Date = mdy(ccpe_numbers$Baseline.Date)
year_one_data = subset(ccpe_numbers, ccpe_numbers$Baseline.Date <"2016/10/01")
dim(year_one_data)
describe.factor(year_one_data$HIV.Status)

```
Year two
```{r}
year_two_data = subset(ccpe_numbers, ccpe_numbers$Baseline.Date >="2016/10/01" & ccpe_numbers$Baseline.Date < "2017/10/01")
dim(year_two_data)
describe.factor(year_two_data$HIV.Status)
```
Year three
```{r}
year_three_data = subset(ccpe_numbers, ccpe_numbers$Baseline.Date >="2017/10/01" & ccpe_numbers$Baseline.Date < "2018/10/01")
dim(year_three_data)
describe.factor(year_three_data$HIV.Status)
```
Year four
```{r}
year_four_data = subset(ccpe_numbers, ccpe_numbers$Baseline.Date >="2018/10/01" & ccpe_numbers$Baseline.Date < "2019/10/01")
dim(year_four_data)
describe.factor(year_four_data$HIV.Status)
```

