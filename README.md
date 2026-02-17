# more_petty_code
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
