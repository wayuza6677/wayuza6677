import requests
from requests.auth import HTTPBasicAuth

def login():
    url = "http://example.com/api/login"  # URL ที่ต้องใช้การเข้าสู่ระบบ
    username = "jungle_queen"
    password = "15072541Wa_"

    # ส่งคำขอ GET พร้อม Basic Authentication
    response = requests.get(url, auth=HTTPBasicAuth(username, password))

    if response.status_code == 200:
        print("Login successful!")
    else:
        print("Login failed with status code:", response.status_code)

login()
