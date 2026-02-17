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
   
