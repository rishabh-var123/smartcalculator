# smartcalculator

response=['Welcome to Smart Calculator Made by-:Rishabh Varshney',
         'My name is Alexa(Daugter of Google)',
         'sorry this is my beyond limit',' Thanks for Enjoy me' ]
def extract_from_text(text):
    l=[]
    
    for t in text.split(' '):
        try:
            l.append(float(t))
        except ValueError:
            pass
    return l
def add(a,b):
    return a+b
def subtract(a,b):
    return a-b
def name():
    print(response[1])
def sorry(): 
    print(response[2]) 
def close():
    print(response[3])
    input("Enter any key to exist")
    exit()
def how():
    print("I am fine and You")
    print("I am a calculator not your girlfriend")
def doing():
    print("Sabge kat rahe hu thu bhi kuch kaam karla bas timepass kar raha ha sala")
def joke():
    print("Aaj Ki Bahu Ka Nara")                       
    print(":- Mera Baccha Saas Sambhale.....")
    print("Saas Ka Baccha Main Sambhal Lungi")
def date():
    from datetime import date
    today = date.today() 
    print("Today's date:", today)
    



operations={'ADD':add,'PLUS':add,'SUBTRACT':subtract,'MINUS':subtract}
commands={'NAME':name ,'HI':name,'END':close,'EXIST':close,'HOW':how,'DOING':doing,'JOKE':joke
          ,'DATE':date}
print("------------"+response[0]+"-----------")
print("------------"+response[1]+"-------------")
# main

while True: 
    print()
    print("May I help u sir --:")
    text=input('enter your queries:  ') 
    for word in text.split(' '): 
        if word.upper() in operations.keys(): 
            try: 
                l = extract_from_text(text) 
                r = operations[word.upper()] (l[0],l[1]) 
                print(r) 
            except: 
                print('something went wrong going plz enter again !!') 
            finally: 
                      break
        elif word.upper() in commands.keys(): 
                      commands[word.upper()]() 
                      break
    else:          
        sorry() 
    

        

                
    
    
      
         
