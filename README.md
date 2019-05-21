# pm-tools
Michael Bernauer

This repository contains scripts for retrieving records from PubMed

## pm-query
This script is used to submit a query to PubMed and can be used to retrieve the
total number of records matching a query or to download the results of a query
in three formats: `medline`, `abstract`, `uilist`. The script accepts a file
containing a PubMed query and results format as input

### Example
```
# get record counts
pm-query -c Geersing_EHR_Sepsis.txt

# download query results in abstract format
pm-query Geersing_EHR_Sepsis.txt abstract

# download pmids for records matching a query
pm-query Geersing_EHR_Sepsis.txt uilist

# download records in medline format
pm-query Geersing_EHR_Sepsis.txt medline
```

## pm-auth
Extracts author names from Medline record

### Example

```
# get medline records for a query and extract authors
pm-query Geersing_EHR_Sepsis.txt medline | pm-auth
```

## pm-mesh
Extracts mesh headings from a Medline record

### Example

```
# get mesh headings for all articles in a query
pm-query Geersing_EHR_Sepsis.txt medline | pm-mesh
```
