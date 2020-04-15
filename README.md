# AndroidStringHelper
This is a tool to convert a CSV file containing translations into localized android xml files

## To import strings from CSV into Android xml format:
  
  python importer.py -i `<inputFile>` -o `<outputDir>` -n [outputFileName] -d [delimiter] -t [strings|plurals|json]
  
  Note: Examples CSV files in the necessary format for both strings and plurals are included in the project.

## To export strings from Android xml to csv:
  
  python exporter.py -i `<resDir>` -o `<outputDir>` -d [delimiter]
  
  Note: The export script currently expects strings and plurals to be kept in separate files.
  
## To compare two Android strings.xml files for missing entries

  csvdiff.py -i `<inputFile1>` -j `<inputFile2>`

# Config options
edit `config.py`
- `has_translations` -- if `True`, export strings that have at least one translation. Default `False`.
- `not_translatable` -- if `True`, export strings that have set `translatable="false"`. Default `False`.
