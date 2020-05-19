# Quotes
The `quote` command group belongs to [`Project Echo`](https://github.com/TCLRainbow/DimBot/projects/1). Use it to interact with the quote database.

## Adding a quote
```
User: d.quote add <message>
DimBot: Quoter?
User: <quoter>
DimBot: Added quote #<index>
```
* **message**: String  
  The actual quote with a maximum character length of 2040.
* **quoter**: String  
  The person who said the quote.
> Note: If DimBot hasn't received `quoter` after 10 seconds, it will ignore this command.

When `quoter` is received, DimBot will add the quote into the database and sends the index of the quote in the database.
## Retrieving a quote
There are multiple ways to retrieve a quote:
* By index
* By quoter
### Retrieving by index
```
d.quote index <quote_index>
```
* **quote_index**: Integer  
  The index of the quote to retrieve.  
  If index is smaller than 1 ,exceeds the quote count in database or simply left empty, DimBot outputs the quote count and randomly picks a quote.