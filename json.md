install.packages("jsonlite")
library(jsonlite)
install.packages("RCurl")
library(RCurl)
totalData <- NULL
roadTotalData <- NULL

-----------------------------
road <- fromJSON(getURL("http://data.taipei/opendata/datalist/apiAccess?scope=resourceAquire&rid=5aacba65-afda-4ad5-88f5-6026934140e6"))
roadTempData <- road$result$results
roadTotalData <- rbind(roadTotalData, roadTempData)

curTime <- Sys.time()
dataCount <- nrow(roadData)
tempData <- merge(curTime, dataCount)
totalData <- rbind(totalData, tempData)
-----------------------------










id <- roadData$SectionId
dataCount <- aggregate(roadData$SectionId~SectionId,roadData,length)
library(knitr)
kable(head(PostCount[order(PostCount$Posts,decreasing = T),],10))

for(i in 1:nrow(PostCount)){
  totalPageLikes <- merge(totalPage, likes, by = "dateDay")
}
