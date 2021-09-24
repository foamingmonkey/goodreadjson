# goodreadjson
 # easy json your own book list from good reads

quick write up on devs version of creating your own book list because good reads took away api :-( amazon bought goodreads like 2 or so years ago.

### Frist you want your own good reads data if you don't have one this is pointless

From good reads click my books and under tools import and export - click export library and it will create a CSV file. 
From the CSV file you will notice it did not import covers (you suck amazon).

1. you want to download csv and take out the data you don't need check out my CSV  
2.  from [openlibrary] (https://openlibrary.org/dev/docs/api/covers) you can pick covers up from http://covers.openlibrary.org/b/isbn/
3.  inside the csv open it in excell or google sheets( if you use google sheets you have to use a merg addon plugin called merge values)
4.  so the next part will depend on if you have excell or google sheets but basiclly you make two new columns call one something like imageurl and paste the http://covers.openlibrary.org/b/isbn/ and simply drag to the last book. the second column will remain blank 
5.   last step will be to combined the ISBN row  with the row called imageurl inside the blank second column for me it was =concatenate(N4,F4,"-L.jpg") on google sheets 

for me this was Quick workaround without API promises and fetch well for me it's easier to work with coming from Shopify dev ( yeah I'm pretty sure there is a easier way to do it) 

https://www.npmjs.com/package/convert-csv-to-json




