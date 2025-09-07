class JuiceMachine:
    def __init__ (self, fruit, water):
        self.fruit = fruit
        self.water = water
    def make_juice(self):
        if self.water >= 300 and self.fruit >= 50:
            self.water -= 300
            self.fruit -= 50
            return True
        else:
            return False

   def add_water(self, amount):
      self.water += amount

   def add_fruit(self, amount):
       self.fruit += amount

   def clean(self):
       if self.water >= 200:
          self.water -= 200
       else:
          self.water = 0





jm = JuiceMachine(1000, 500)  # 1000 g frukt, 500 ml vatten

if jm.make_juice():
    print("One glass of juice is ready!")

jm.clean()
jm.add_water(100)
jm.add_fruit(50)

if jm.make_juice():
    print("Another glass of juice is ready!")
