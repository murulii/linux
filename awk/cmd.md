```
Diff b/w awk and SED
Awk is used to format a data and filter a data on file
sed is used to edit stramming data or ouput

awk '' filename.txt
awk '{print}' filename.txt
awk '{print $1,$2}' filename.txt //Display colum 1 and 2 
awk '/muruli/ {print $1}' file.txt //Find muruli and print coulm 1 data
awk '/muruli/ {count++} END {print count}' file.txt //Count how many times muruli came
awk '/muruli/ {count++} END {print "the count is ", count}' file.txt //Find the count
awk '$2 >= "08:23" && $2 <= "08:25" {print $2,$3,$4}' file.txt  //Display the data that time b/w 8:23 to 8:25 and print it the 2 3 4 colums
```
