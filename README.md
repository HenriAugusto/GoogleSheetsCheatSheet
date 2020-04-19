# GoogleSheetsCheatSheet
Useful stuff for google sheets

## Conditional Formatting

### Finding duplicates

_Used with conditional formatting this will color the entire line where there is a duplicate on the selected column_

- If you have a google forms for enrollments/subscriptions/registrations/etc it makes it easier to find people who did the process more than once.
- Useful for any forms because sometimes users double click the "send" button and the form receives two identical responses

Replace B with the column

`=COUNTIF($B:$B;$B1)>1`

- PT-BR= `CONT.SE()`

Replace **B** with the column where you want to find the duplicates.

If you want to highlight the first instance with a different color you can use the following formula (with a higher priority)

`=AND( COUNTIF($H:$H; $H1) >1 ; COUNTIF($H$1:$H1; $H1) =1 )`

and for the rest

`=AND( COUNTIF($H:$H; $H1) >1 ; COUNTIF($H$1:$H1; $H1) > 1 )`

## Misc

### Strings

[Count cells containing string in any position](https://stackoverflow.com/questions/17152704/google-spreadsheet-count-if-contains-a-string)
