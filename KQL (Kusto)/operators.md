#search #where #take #count #summarize #extend #project #distinct #top

## Search

search -> search all columns in "Table" for the value "string ", by default is not case sensitive
eg:
Perf - this a tabl
| search "Memory" - will look for "Memory" |
| ---------------------------------------- |
to make this query case sensitive use search kind=case_sensitive

we can search accros all table 
search "Memory"
or search accros multiple tables:
search in (Perf, Event Alert ) "Memory "

Searching specyfic columne 
Perf 
| search CounterName == "Available MBytes" |
| ---------------------------------------- |

Serching for value in the column 
Perf 
| search CounterName : "MBytes" |
| ----------------------------- |
|                               ||
we can use "\*something \*" to search for the wild cards

when we want to serach values in column that starts/end with specyfic "string"

Perf 
search * startwith/endswith "Bytes"

## where
where  limist the query result sets, it is the condition that have to be fullfiled to display results. 
Often used with time 
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/samples?pivots=azuremonitor&toc=%2Fazure%2Fazure-monitor%2Ftoc.json#date-time-basics -> time syntx 

you can have multiple where in one KQL query 

You can simulate search using where:
Perf
where *  has "string"

"haspreffix" and "hassuffix" is similarch to search "startswith"/"endswith"

we can also use "contains" or regex 
## Take 
take is used to grab random number of data from the input rows
if we run same query 2 times there is no guarantee that returned results will be the same
most ofen used to check if query works corectly 
works with other langage operators

you can use take and limit interchangable



## Count
return number of rows that are in the dataset, can be used with other operators

## Summarize
summarize gives you the summury output , can be braked down by multiple columns
eg:
Perf 
| summarize  count() by InstanceName, ObjectName |
| ---------------------------------------------- |
| 
|
in abowe case we will get in our output as one of the columns count_ if we want to rename this column we can use this sintax:
Perf 
| summarize  PerfCount=count() by InstanceName, ObjectName |

## Extend
extend create calculated columne and adds it the result outpout 
Perf
where ColName == "Some value"
exdend NewColName = ColName / 1000

## Project
project allows you to display subset of columnt to the output window

project can simulate extend -> we can calculate new columns in with project

in project-away we can remove columns from our display output

if we want to rename column we can use project-rename 
project-rename newName = oldName



## Distinct
distinct returns a list of deduplicated vauls for columns from input dataset