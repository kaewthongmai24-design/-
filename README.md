import time
import os
import random

def memory_game():
    # สุ่มตัวเลข 5 หลัก
    secret_number = str(random.randint(10000, 99999))
    
    print("--- แอปทดสอบความจำระยะสั้น ---")
    print(f"จำตัวเลขนี้ให้ดี: {secret_number}")
    
    # ให้เวลาจำ 3 วินาที
    time.sleep(3)
    
    # ล้างหน้าจอ (สำหรับ Windows ใช้ 'cls' สำหรับ Mac/Linux ใช้ 'clear')
    os.system('cls' if os.name == 'nt' else 'clear')
    
    print("ตัวเลขเมื่อกี้คืออะไร?")
    answer = input("คำตอบของคุณ: ")
    
    if answer == secret_number:
        print("เก่งมาก! ความจำเธอแม่นยำสุดๆ ✅")
    else:
        print(f"ว้า... เกือบถูกแล้ว ตัวเลขที่จริงคือ {secret_number} ❌")

if __name__ == "__main__":
    memory_game()
