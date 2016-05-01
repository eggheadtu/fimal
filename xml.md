install.packages("XML")
library(XML)

fileUrl<-"http://www.dgbas.gov.tw/public/data/open/Cen/Mp04018.xml"
doc<-xmlTreeParse(fileUrl,useInternal=TRUE)
rootNode<-xmlRoot(doc)
xmlName(rootNode)
rootNode

xpathSApply(rootNode,"//Year_and_month",xmlValue)

rootNode[[1]]
