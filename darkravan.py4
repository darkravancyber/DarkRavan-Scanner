import os
import socket
import threading
import time

# 🔥 Banner
os.system("clear")
print("""
\033[91m==============================
|  DARK-RAVAN PORT SCANNER ⚔️ |
==============================\033[0m
""")

# 🔘 Menu
print("1. Basic Scan")
print("2. Pro Scan (Fast)")
choice = input("\nChoose option (1/2): ")

target = input("Enter target IP/Host: ")

def basic_scan(target):
    print(f"\n\033[94m[~] Starting Basic Scan on {target}...\033[0m")
    for port in range(1, 100):
        try:
            s = socket.socket()
            s.settimeout(0.5)
            s.connect((target, port))
            print(f"\033[92m[+]\033[0m Open port: {port}")
            s.close()
        except:
            pass

def pro_scan(target):
    print(f"\n\033[94m[~] Starting Pro Scan on {target}...\033[0m")
    def scan(p):
        try:
            s = socket.socket()
            s.settimeout(0.3)
            s.connect((target, p))
            try:
                service = socket.getservbyport(p)
            except:
                service = "Unknown"
            print(f"\033[92m[+]\033[0m Port {p} open → {service}")
            s.close()
        except:
            pass
    for port in range(1, 100):
        t = threading.Thread(target=scan, args=(port,))
        t.start()

# 🔁 Run based on input
if choice == '1':
    basic_scan(target)
elif choice == '2':
    pro_scan(target)
else:
    print("\033[91m[-] Invalid choice\033[0m")
ls
README.md  LICENSE  portscanner.py  portscanner_pro.py  darkravan.py



