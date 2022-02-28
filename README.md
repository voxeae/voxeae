import requests
import uuid
import secrets
import time
import os
orr="\033[0;91m"
yell="\033[0;93m"
gr = "\033[0;92m"
print(yell)
line = "-------------------#GZ~«@gzwi.sw»--------------------\n"
logo = f"""

Bot From «@gzwi.sw» in Instagram
"""
a = 1
r = requests.Session()
u = uuid.uuid4()
print(orr)
print(logo)
print(yell)
print(line)
print("[1]Spam")
print("[2]Self injury")
print("[3]Sale of illegal or regulated goods")
print("[4]Nudity or sexual activity")
print("[5]Violence or dangerous organizations")
print("[6]Hate speech or symbols")
print("[7]Bullying or harassment")
print("[8]preteding someone i know")
print("[11]under the age of 13")
print("[12]Sale Guns")
print("[13]pretending me")
print(line)
print("     ")
repo = int(input("[$]Enter The Num Of Report :>> "))
user = input("[$]YOUR U$ERNAME  :>> ")
password = input("[$]YOUR PA$$WORD :>> ")
target = input("[$]THE TARGET :>> ")
z = int(input("[$]The Sleep :>> "))
much = int(input("[$]How Much The Bot Report? :>> "))


b = 'https://www.instagram.com/accounts/login/ajax/'

w = {
"accept":"*/*",
"accept-encoding":"gzip, deflate,br",
"accept-language": "ar,en-US;q=0.9,en;q=0.8",
"content-length": "279",
"content-type": "application/x-www-form-urlencoded",
"origin": "https://www.instagram.com",
"referer": "https://www.instagram.com/",
"sec-fetch-dest":"empty",
"sec-fetch-site":"same-origin",
"user-agent":"Mozilla/5.0 (Windows NT 10.0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/85.0.4183.83 Safari/537.36",
"x-csrftoken": "lih2ypMfhzdqwMbm5jIILqxZDj4zLeCW",
"x-ig-app-id": "936619743392459",
"x-ig-www-claim": "hmac.AR1_p9SjMFQF73bcZgzygDgxb9yBZUn83e69xoDD2qpSdmtW",
"x-instagram-ajax":"901e37113a69",
"x-requested-with":"XMLHttpRequest"
}

k = {'username':user,
            'enc_password':
'#PWD_INSTAGRAM_BROWSER:0:1589682409:{}'.format(password),
            'queryParams': '{}',
            'optIntoOneTap': 'false',}

l = r.post(b,headers=w,data=k)

if("userId") in l.text:
 r.headers.update({'X-CSRFToken': l.cookies['csrftoken']})
 print("log true")
 
 v = "https://www.instagram.com/{}/?__a=1".format(target)
 t = r.get(v).json()
 y = str(t["logging_page_id"])
 h = y.split("_")[1]
 for i in range(much):
  urreport = "https://www.instagram.com/users/{}/report/".format(h)
  dat = {f'source_name':'','reason_id':{repo},'frx_context':''}
  repp = r.post(urreport,data=dat)
  os.system("clear")
  print(f"{logo}\n{yell}\n{line}\n[$]The Target : {target} \n[$]The Sleep : {z} \n[$]Done Report : {a}\n[$]The Number of reports : {much}\n\n{line}")
  time.sleep(z)
  a += 1
 
