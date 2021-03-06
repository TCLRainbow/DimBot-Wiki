# Key terms
## Uploader
A Discord user who uploaded the quote

## Quoter
Quoter means the person who said the quote. However, quoters can be grouped.

Quoter's format: `[Quoter], [QuoterGroup]`

Consider the following examples:
> Stay hungry, stay foolish. - Steve Jobs  
> I love Dim - Kingsman, Dim's server  
> Someone loves Dim - , Dim's server

`Steve Jobs` and `Kingsman` are quoters. `Dim's server` is the quoter group.
> Note: You can specify just the quoter group by `, <QuoterGroup>`

This allows an uploader to give context for a quote. A common use case of quoter group is the name of an anime, with quoter being a character within the anime.

# Commands
## Adding a quote
alias: `d.quote a`
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
> **Note: If DimBot hasn't received `quoter` after 10 seconds, it will ignore this command.**

When `quoter` is received, DimBot will add the quote into the database and sends the index of the quote in the database.
## Retrieving a quote
There are multiple ways to retrieve a quote:
* By index
* By quoter
* By uploader
### Retrieving by index
alias: `d.quote i`
```
d.quote index <index>
```
* **index**: Integer  
  The index of the quote to retrieve.  
  If index is smaller than 1 ,exceeds the quote count in database or simply left empty, DimBot outputs the quote count and randomly picks a quote.
### Retrieving by quoter
alias: `d.quote q`
```
d.quote quoter <quoter>
```
* **quoter**: String  
  The quoter to search
### Retrieving by uploader
alias: `d.quote u`
```
d.quote uploader <user>
```
* **user**: Discord User  
  This can be anything that can represent a discord user, usually the user's ID or username.
## Deleting a quote
alias: `d.quote d`, `d.quote del`
```
d.quote delete <quote_index>
```
* **index**: Integer  
  The index of the quote to delete.