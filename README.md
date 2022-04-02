### IOS - Project 1
Processes data in `.csv` files from [mzcr.cz](https://onemocneni-aktualne.mzcr.cz/api/v2/covid-19)  
  
The format of data in `.csv` files have to be in this form:  
`id,datum,vek,pohlavi,kraj_nuts_kod,okres_lau_kod,nakaza_v_zahranici,nakaza_zeme_csu_kod,reportovano_khs`  
  
The script supports only files of type `.csv`, `.csv.gz` and `.csv.bz2`.  

Usage `./corona [-h] [FILTERS] [COMMAND] [LOG [LOG2 [...]]` or `./corona -h` for more info.  
  
Running the script takes some time to process the data depending on the performance of the computer. 
You may try to run the script with `time curl -s https://onemocneni-aktualne.mzcr.cz/api/v2/covid-19/osoby.csv | ./corona -s 15 age`
and see, how long it takes *(tested on 3 devices with newer CPUs and it did not take longer than a minute)*.
