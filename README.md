import time

class Cultivator:
    def __init__(self, name, cultivation_level=1, energy=100):
        self.name = name
        self.cultivation_level = cultivation_level
        self.energy = energy

    def cultivate(self):
        print(f"{self.name}开始修炼...")
        time.sleep(2)  # 模拟修炼过程
        self.energy += 10
        self.cultivation_level += 1
        print(f"{self.name}修炼完成，能量+10，修为+1")

    def meditate(self):
        print(f"{self.name}开始冥想...")
        time.sleep(1)  # 模拟冥想过程
        self.energy += 5
        print(f"{self.name}冥想完成，能量+5")

    def status(self):
        print(f"修仙者 {self.name} 当前状态：")
        print(f"修为等级: {self.cultivation_level}")
        print(f"能量: {self.energy}")

# 示例使用
player1 = Cultivator("王小明")

# 修炼和冥想
player1.cultivate()
player1.meditate()

# 打印状态
player1.status()
