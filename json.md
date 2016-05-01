install.packages("jsonlite")
library(jsonlite)

install.packages("RCurl")
library(RCurl)

BusTime<-fromJSON(getURL("http://data.ntpc.gov.tw/api/v1/rest/datastore/382000000A-000269-002"))
Bus<-BusTime$result$records
Bus

CarTime<-fromJSON(getURL("http://data.ntpc.gov.tw/api/v1/rest/datastore/382000000A-000357-001"))
Car<-CarTime$result$records
Car

TrainTime<-fromJSON(getURL("http://163.29.3.98/json"))
Train<-TrainTime$result$records
Train

Road<-fromJSON(getURL("http://data.taipei/opendata/datalist/apiAccess?scope=resourceAquire&rid=5aacba65-afda-4ad5-88f5-6026934140e6"))
RoadData<-Road$result$results
RoadData
