import os
import random
import string
import time

def display_banner():
    print(r"""
__     ________        ___    ____  ____  _____ _   _ 
\ \   / / ___\ \      / / \  |  _ \|  _ \| ____| \ | |
 \ \ / / |  _ \ \ /\ / / _ \ | |_) | | | |  _| |  \| |
  \ V /| |_| | \ V  V / ___ \|  _ <| |_| | |___| |\  |
   \_/  \____|  \_/\_/_/   \_\_| \_\____/|_____|_| \_|
                                                       
                          https://vgwarden.vercel.app
    """)

def generate_random_string(length=100):
    return ''.join(random.choices(string.ascii_letters + string.digits, k=length))

def create_edit_delete_file():
    folder_name = "24-7"
    os.makedirs(folder_name, exist_ok=True)

    while True:
        try:
            file_name = f"{folder_name}/{generate_random_string(8)}.txt"
            num_lines = random.randint(10, 100)
            
            with open(file_name, "w") as file:
                for _ in range(num_lines):
                    random_content = generate_random_string(100)
                    file.write(random_content + "\n")
            
            time.sleep(2)
            
            with open(file_name, "w") as file:
                num_lines = random.randint(10, 100)
                for _ in range(num_lines):
                    random_content = generate_random_string(100)
                    file.write(random_content + "\n")
            
            time.sleep(1)
            
            os.remove(file_name)

            time.sleep(1)
        
        except Exception:
            time.sleep(5)

if __name__ == "__main__":
    display_banner()
    create_edit_delete_file()
