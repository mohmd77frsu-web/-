الصطوره قيصر 
# القيصر
import sys
import logging
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.chrome.options import Options

logging.basicConfig(level=logging.INFO, format='%(message)s')

class AlQaisarFramework:
    def __init__(self):
        # تم دمج الواجهتين بشكل متناسق
        self.banner = r"""
88888888888888888888888888888888888888888888888888888888888888888888888
88.._|      | `-.  | `.  -_-_ _-_  _-  _- -_ -  .'|   |.'|     |  _..88
88   `-.._  |    |`!  |`.  -_ -__ -_ _- _-_-  .'  |.;'   |   _.!-'|  88
88      | `-!._  |  `;!  ;. _______________ ,'| .-' |   _!.i'     |  88
88..__  |     |`-!._ | `.| |_______________||."'|  _!.;'   |     _|..88
88   |``"..__ |    |`";.| i|_|MMMMMMMMMMM|_|'| _!-|   |   _|..-|'    88
88   |      |``--..|_ | `;!|l|MMoMMMMoMMM|1|.'j   |_..!-'|     |     88
88   |      |    |   |`-,!_|_|MMMMP'YMMMM|_||.!-;'  |    |     |     88
88___|______|____!.,.!,.!,!|d|MMMo * loMM|p|,!,.!.,.!..__|_____|_____88
88      |     |    |  |  | |_|MMMMb,dMMMM|_|| |   |   |    |      |  88
88      |     |    |..!-;'i|r|MPYMoMMMMoM|r| |`-..|   |    |      |  88
88      |    _!.-j'  | _!,"|_|M<>MMMMoMMM|_||!._|  `i-!.._ |      |  88
88     _!.-'|    | _."|  !;|1|MbdMMoMMMMM|l|`.| `-._|    |``-.._  |  88
88..-i'     |  _.''|  !-| !|_|MMMoMMMMoMM|_|.|`-. | ``._ |     |``"..88
88   |      |.|    |.|  !| |u|MoMMMMoMMMM|n||`. |`!   | `".    |     88
88   |  _.-'  |  .'  |.' |/|_|MMMMoMMMMoM|_|! |`!  `,.|    |-._|     88
88  _!"'|     !.'|  .'| .'|[@]MMMMMMMMMMM[@] \|  `. | `._  |   `-._  88
88-'    |   .'   |.|  |/| /                 \|`.  |`!    |.|      |`-88
88      |_.'|   .' | .' |/                   \  \ |  `.  | `._-Lee|  88
88     .'   | .'   |/|  /                     \ |`!   |`.|    `.  |  88
88  _.'     !'|   .' | /                       \|  `  |  `.    |`.|  88
    
    [ القيصر اليمني - Al-Qaisar Al-Yamani ]

             _
       / \      _-'
     _/|  \-''- _ /
__-' { |          \
    /             \
    /       "o.  |o }
    |            \ ;
                  ',
       \_         __\
         ''-_    \.//
           / '-____'
          /
        _'
      القيصر اليماني
        """

    def display_banner(self):
        print(self.banner)

    def initialize_driver(self):
        try:
            chrome_options = Options()
            chrome_options.add_argument("--headless")
            chrome_options.add_argument("--no-sandbox")
            chrome_options.add_argument("--disable-dev-shm-usage")
            service = Service()
            return webdriver.Chrome(service=service, options=chrome_options)
        except Exception as e:
            logging.error(f"[!] خطأ أثناء تشغيل المتصفح: {e}")
            return None

    def run(self):
        self.display_banner()
        logging.info("[+] تم تحميل إطار القيصر اليمني بنجاح.")
        logging.info("[!] النظام جاهز للعمل.")
        
if __name__ == "__main__":
    app = AlQaisarFramework()
    app.run()
