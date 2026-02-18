# more_petty_code
#for document files
jay = open('jacobo.txt','r') #r- is to read
say = jay.read()
print(say) #for opening a text file in python
jay.close() #to close the file 

with open('code.txt','w') as fine: #w -is to write
   fine.write('Mucho Gracias Amigo,\n')
   fine.write('Mucho Gracias Amiga,\n')#each new line as to start like this
   fine.write('Mucho Gracia Amigo,\n')
   fine.write('Much Gracias Amigo,\n')
   fine.write('thanks.\n')

with open('code.txt','a') as fine: #a is to append ie add to w because each time w runs its overwrites previous script
    fine.write('THIS was added,\n')
    fine.write('Muy,\n')
    fine.write('thanks.\n')

additional_lines =['First line is,\n','Second line added'] #THIS IS A BETTER WAY TO ADD THINGS WITHOUT MULTIPLE REENTRIES, IT USES []LISTS
with open('code.txt','a') as fine:
    fine.writelines(additional_lines)
    
FOR CSV FILES


import csv
with open('mycsv.csv','r') as excsv: #for csv files always remember to add the format of the file .csv
    csv_reader = csv.reader(excsv)
    
    
    for row in csv_reader:
        print(row)
----
import csv
with open('mycsv.csv','r') as excsv:
    csv_reader = csv.reader(excsv)
    
    
    for row in csv_reader:
        
        print(row)

to print individual rows

with open('mycsv.csv','r') as excsv:
    csv_reader = csv.reader(excsv)
    next(csv_reader) #this is to remove the header from appearing in the results, it can be removed if not needed.
    
    for row in csv_reader:
        Name = row[0] #index starts at 0
        age = row[4]
        print(Name)
        print(age)
        # to print into sentence# print(f'my name is {Name};I'm {age}.')

#to write csv file

import csv

data = [
    ["name", "age", "city", "score", "active", "signup_date", "favorite_color", "notes"],
    ["Emma", 24, "Oslo", 87.5, True, "2024-03-12", "teal", "prefers night shifts"],
    ["Liam", 31, "Berlin", 64.0, False, "2023-11-30", "navy", ""],
    ["Sofia", 19, "Lisbon", 92.3, True, "2025-01-08", "coral", "allergic to nuts"],
    ["Noah", 45, "Tokyo", 41.8, True, "2022-05-19", "gray", "very punctual"],
    ["Ava", 28, "Austin", 78.9, False, "2024-07-01", "purple", "left early last week"],
    ["Lucas", 33, "Toronto", 55.2, True, "2023-09-14", "green", ""],
    ["Mia", 22, "Sydney", 95.1, True, "2025-02-03", "pink", "loves coffee"],
    ["Ethan", 39, "Madrid", 72.4, False, "2021-12-25", "orange", "needs new laptop"],
    ["Isabella", 27, "Seoul", 88.7, True, "2024-10-17", "violet", ""],
    ["James", 52, "Chicago", 19.5, False, "2020-04-02", "brown", "retiring soon"],
    ["Olivia", 20, "Cape Town", 81.6, True, "2025-01-29", "mint", "very quiet"],
    ["Benjamin", 36, "Barcelona", 66.9, True, "2023-06-11", "indigo", "plays guitar"],
    ["Charlotte", 25, "Vancouver", 90.2, False, "2024-08-20", "lavender", ""],
    ["Alexander", 41, "Dublin", 53.4, True, "2022-02-14", "red", "hates Mondays"]
 ]  

with open('practice_data.csv', 'w', newline='', encoding='utf-8') as f:
    writer = csv.writer(f)
    writer.writerows(data)

print("CSV file created!")

another way =>

import csv

with open('flint.csv','w',newline='') as stone: #newline='' removes extra spaces between the header and rest of the table
    csv_writer = csv.writer(stone)
    
    csv_writer.writerow(["name", "age", "city", "score", "active", "signup_date", "favorite_color", "notes"]) # .writerow is for adding headers
    csv_writer.writerow(["Alexander", 41, "Dublin", 53.4, True, "2022-02-14", "red", "hates Mondays"])

     csv_writer.writerows([ ["Emma", 24, "Oslo", 87.5, True, "2024-03-12", "teal", "prefers night shifts"],
    ["Liam", 31, "Berlin", 64.0, False, "2023-11-30", "navy", ""],
    ["Sofia", 19, "Lisbon", 92.3, True, "2025-01-08", "coral", "allergic to nuts"],
    ["Noah", 45, "Tokyo", 41.8, True, "2022-05-19", "gray", "very punctual"],
    ["Ava", 28, "Austin", 78.9, False, "2024-07-01", "purple", "left early last week"],
    ["Lucas", 33, "Toronto", 55.2, True, "2023-09-14", "green", ""],
    ["Mia", 22, "Sydney", 95.1, True, "2025-02-03", "pink", "loves coffee"],
    ["Ethan", 39, "Madrid", 72.4, False, "2021-12-25", "orange", "needs new laptop"],
    ["Isabella", 27, "Seoul", 88.7, True, "2024-10-17", "violet", ""],
    ["James", 52, "Chicago", 19.5, False, "2020-04-02", "brown", "retiring soon"],
    ["Olivia", 20, "Cape Town", 81.6, True, "2025-01-29", "mint", "very quiet"],
    ["Benjamin", 36, "Barcelona", 66.9, True, "2023-06-11", "indigo", "plays guitar"],
    ["Charlotte", 25, "Vancouver", 90.2, False, "2024-08-20", "lavender", ""],
    ["Alexander", 41, "Dublin", 53.4, True, "2022-02-14", "red", "hates Mondays"]]) #this is to add multiple rows at once, it uses .writerows instead of .writerow

   
