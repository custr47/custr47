- 👋 Hi, I’m @custr47
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
custr47/custr47 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import requests, random, datetime
from colorama import Fore
R = Fore.RED
P = Fore.GREEN
s = Fore.LIGHTRED_EX
y = Fore.YELLOW
fz = datetime.datetime.now()
print(y+f"""
**********************************
*  {fz}    *                                                                   
*                                *                                               
* - [ Checker TiKTok V.507 ] -   *
*                                *
* Tool developer -> : @Filza_507 *
* Channel TeleGram -> : @TweakPY * 
**********************************
""")
sa="4"
if sa =="4":
    uesr = ''   
    chars2 = 'qwertyuiopasdfghjklzxcvbnm1234567890._'
    amount = 5000
    amount = int(amount)

    length2 = 4
    length2 = int(length2)

    for password in range(amount):
        password = ''

        for item in range(length2):
            password = ''
        for item in range(length2):
            password += random.choice(chars2)

        
        with open('user.txt', 'a') as x:
            x.write(uesr + password + '\n')
j = requests.get('https://pastebin.com/raw/jsXm5HCA').text
x2 = requests.get('https://pastebin.com/raw/08NqbfeS').text
use="user.txt"
ID = input(R+"Enter Your id Account -> :")
token = input(R+'EnTer Your Token ->:')
headers={
"accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9",
"user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.141 Safari/537.36",
"Connection": "close",
"Host": "www.tiktok.com",
"Accept-Encoding": "gzip, deflate",
"Cache-Control": "max-age=0"}
file = open(use, "r")
while True:
	Check = file.readline().split('\n')[0]
	if Check == '':
		break
	tiklog = f'https://www.tiktok.com/@{Check}'
	rq = requests.get(tiklog, headers=headers)
	if rq.status_code == 404:
		print(P+'[+] Available >> {}'.format(Check))
		tele = (
			f'https://api.telegram.org/bot{token}/sendMessage?chat_id={ID}&text={j}\n𖡃 𝚄𝚂𝙴𝚁:{Check}\n{x2}')
		re = requests.post(tele)
		with open('Tik-HuNt.txt', 'a') as x:
			x.write(Check + '\n')
	elif rq.status_code == 200:
		print(s+'[-] NoT Available >> {}'.format(Check))


