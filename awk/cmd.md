```
Diff b/w awk and SED
Awk is used to format a data and filter a data on file and its works on structured data like csv,tsv
sed is used to format a data and used to edit stramming data or ouput adn it works on line by line if it is structured or un strucred
sed using we can replace data
```
**AWK**
```
awk '' filename.txt
awk '{print}' filename.txt
awk '{print $1,$2}' filename.txt //Display colum 1 and 2 
awk '/muruli/ {print $1}' file.txt //Find muruli and print coulm 1 data
awk '/muruli/ {count++} END {print count}' file.txt //Count how many times muruli came
awk '/muruli/ {count++} END {print "the count is ", count}' file.txt //Find the count
awk '$2 >= "08:23" && $2 <= "08:25" {print $2,$3,$4}' file.txt  //Display the data that time b/w 8:23 to 8:25 and print it the 2 3 4 colums
```
**SED**
```
sed '' file.txt
sed -n '/info/p' file.txt        // "-n" is used to match/filter exact cahracter ex "info" and "p" used to print

sed 's/info/g' file.txt  // "s" means sub string change a sub string data and "g" Globally change all data   
sed -n -e '/info/=' file.txt //print which line contain info "-e" expression -n "=" means showing line number
sed -n -e '/info/=' -e '/info/' file.txt //print which line contain info "-e" expression -n "=" means showing line number and with coulm 2 nd expression gives
```

**Grep**

i want to find data thats runs on process ps
we can grep the output displayed ex ps aux | grep cpu
```
grep -i -c info file.txt //seach info "-i" casesenstive and non casesensitive data and  "-c" count
```
