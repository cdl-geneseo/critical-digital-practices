---
title: Data Quality
layout: default
parent: Working with Data
nav_order: 5
---
# Data Quality

Some obstacles to quality that we may encounter in raw or processed data include:

- Missing values (e.g., empty spreadsheet cells, `,,` in a CSV file)
- Multiple formats for the same value (e.g., "yes", "y", and "1" used interchangeably for a positive survey response)
- Suspect values (e.g. a date of birth recorded as "00/11/1234" or a person's age recorded as "-37")
- Duplicate records/observations (two identical rows that don't represent two different records/observations)
- Dubious outliers (e.g., a temperature reading of "95" for a date in February when temperatures recorded for all other dates that month range from "0" to "42")

## Attribues of high quality data

High quality data possesses **validity**, **accuracy**, **completeness**, **consistency**, and **uniformity**.  When a data set lacks one or more of these attributes, we can sometimes, but not always, improve it through data cleaning.

### Validity

For data to be valid, records/observations should in general:

- Use the same format for a given value. In the example above, any of "yes", "y", or "1" could serve as the value for a positive survey response. Cleaning would involve selecting one format and changing any differently formatted instances of the same value to match the selected one.
- Not contain (for scientific data) observations with empty values. In some contexts, cleaning may involve replacing empty values with a consistently used placeholder value. In other contexts, it may involve deleting the whole record/observation in question from the data set.
- Be unique. A temperature value for two successive days may be the same if the two observations in question represent unique measurements that produced the same result. On the other hand, two records for different individuals containing identical values for the variable "Social Security Number" is a problem that needs addressing.

### Accuracy

For data to be accurate, the values in records/observations must be accurate. Validity and accuracy are not the same. "123 Notrealia St., Erewhon, IA 98201" would be a *valid* value for an address if it conforms to the format chosen for recording addresses in the data set. But since no such address exists, it wouldn't be an *accurate* value.

For scientific data, accuracy must generally be produced through careful observation rather than cleaning. For some other kinds of data, it may be possible to correct inaccuracies by cross-referencing trusted external sources. A data set of government buildings that gave "1600 Pennsylvania Avenue NW, Washington, DC 50200" as the address of "White House" would contain an inaccurate value, since the actual zip code is "20500". It would probably be reasonable to clean the inaccuracy manually.

### Completeness

For data to be complete, it must represent everything that could be known for the context in question. Completeness, like accuracy, is mainly achieved in the data collection process itself, through careful observation of phenomena or thorough recording of information.

### Consistency

For data to be consistent, the values in different records/observations must not be in contradiction. A data set of temperature observations with two observations showing identical values for all variables (e.g., "Location", "Date", "Time", "Instrument") but two different values for "Temperature" would present a consistency problem. 

### Uniformity

For data to be uniform, the same unit of measure must be used in all relevant measurements. In a data set of body measurements, if the value of "Height" is sometimes given in meters and sometimes in feet and inches, cleaning would involve choosing one type of measure and converting all values to that type.

## Manual vs. programmatic data cleaning

Some data cleaning must be done manually. The more we can correct errors programmatically, however, the more time we'll save and the less likely we'll be to miss errors by overlooking them.

Programmatic approaches include search/replace strategies within plain text files (likely to be most effective when they employ [regular expressions](https://www.computerhope.com/jargon/r/regex.htm)), methods and functions available in programming languages, and features available within spreadsheet applications. When you open a data set in Google Sheets, for example, the software may prompt you with an offer to help clean your data and suggest steps to solve problems like those listed above.

When cleaning data programmatically, there's always a risk we'll accidentally corrupt the data by adopting an algorithm that catches more in its net than we intended. We may need to take a few trial runs with a programmatic approach before we're confident that we'll be making intended changes only. This is a good time for a general reminder that you should regularly [back up all your stuff]({{ site.url }}/before-you-start#back-up-your-stuff). In addition, it's a good idea to make a quick backup copy of a data set immediately before making programmatic changes to it. To avoid losing track of which file is the working copy and which is the backup, adopt a regular system of naming backups. One good system is to attach a date and time stamp directly to the file name: e.g., `mydata_backup_2023-08-16_08-15.csv`.
