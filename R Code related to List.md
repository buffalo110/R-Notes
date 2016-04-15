# R Code related to List

Compare to data frame, list is somewhat harder to operate on. However, when querying data from API, the format is usually list. So it's 
important to know how to deal with lists. 

Delete one sublist from a list:

`
 l<- lapply(myList, function(x) dplyr::select(x, -subList))
`
 
Get column names of data frame in list:

`
l<- unique(unlist(lapply(myList, base::names)))
`

Delete a column from data frame in list:

`
l<- lapply(myList, function(x) { x["columnname"] <- NULL; x })
`
