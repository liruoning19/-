import xml.etree.ElementTree as ET
import random

def guess_the_number(x1, x2, max_attempts):
    target_number = random.randint(x1, x2)
    attempts = 0

    while attempts < max_attempts:
        guess = int(input(f"請猜一個介於 {x1} 和 {x2} 之間的數字："))
        attempts += 1

        if guess < target_number:
            print("太低了！")
        elif guess > target_number:
            print("太高了！")
        else:
            print(f"恭喜！你猜對了，目標數字就是 {target_number}！")
            break

    if attempts == max_attempts:
        print(f"很抱歉，你已經猜了{ target_number  }次，但沒有猜中。目標數字是 {target_number}。")

# 解析XML檔案
tree = ET.parse('setting.xml')
root = tree.getroot()

# 從XML中獲取參數
min_range = int(root.find('range/min').text)
max_range = int(root.find('range/max').text)
max_attempts = int(root.find('max_attempts').text)

guess_the_number(min_range, max_range, max_attempts)