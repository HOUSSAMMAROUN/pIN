# pIN
from colorama import Fore
import qrcode
import datetime
g = Fore.RED
df = datetime.datetime.now()
m = df.month;y = df.year
d = df.day;h = df.hour
#--------------------------------------------------------------------------
try:
    print ("Family and personal names must begin with a large letter")
    er = str(input("Fristname:"))
    re = str(input("familyname:"))
    k = 'hello! '+er+" "+re
    print(str(k))
    b =int(input("yourage:"))
    fg = str(y-b)
    j = y-b
    j = str(j)
    i = input("So your year is:"+j+" --yes or no-->")
    if i=="no":
         B=int(input("yoryear:"))
    if i=="yes":
        pass
    pr=input("YourEmail: ")
    if "@gmail.com" in pr:
        pass
    else:
        del pr
    plo = input("passwordEmail: ")
    try:
        rt = "FristName: "+er+", FamilyName: "+re+", age:  "+str(b).upper()+" ,Email:"+pr+" ,password: "+plo
        text = str(rt)
        file = open('/storage/emulated/0/Pp/dat.txt','w')
        file.write(text)
        ffo = qrcode.make(rt)
        F = "/storage/emulated/0/Pp/"
        R=input("Do you want to save this information in QR code and txtFile-->")
        if R=="yes":
            ffo.save(F+"fo.png")
            file.close()
       
        else:
            del ffo
    except:
        print(g,"Error in  information!!! ")
except:
    x = 20
    for jx in range(x):
        print(g,"Error!!!!!")
print(Fore.WHITE)  
