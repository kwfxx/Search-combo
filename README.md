import requests
import threading
import random
ab=0
def gen():
    global ab
    while True:
        headers = {
            'user-agent': 'Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/132.0.0.0 Mobile Safari/537.36',
        }        
        data = {
            'variables': '{"data":{"chaining_mode":"same_author","clips_media_id":null,"page_size":15},"first":null}', 
            #'server_timestamps': 'true'
            'doc_id': '8993519360741225'
        }        
        response = requests.post('https://www.instagram.com/graphql/query', headers=headers, data=data).json() 
        usernames = set([us['node']['media']['user']['username'] for us in response['data']['xdt_api__v1__clips__clips_on_logged_out_connection_v2']['edges']])              
        for user in usernames:
              pas= [
                  "123456",
    "12345@@",
     user,
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
              print(f'''
                {ab} / {user} / {pasw}
  ''')
  
              ab+=1
              with open('combo.txt', 'a') as f:
              	f.write(f'{user}:{pasw}'+'\n')
            
for i in range(3):
  threading.Thread(target=gen).start()
