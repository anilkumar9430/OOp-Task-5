# OOp-Task-5

# ques 1:
class Shape:

    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def _init_(self, radius):
        self.radius = radius

    def area(self):
        return (pi*pow(self.radius,2))

class Square(Shape):
    def _init_(self, edge):
        self.edge = edge

    def area(self):
        return pow(self.edge, 2)

class Rectangle(Shape):
    def _init_(self, length, breadth):
        self.length = length
        self.breadth = breadth

    def area(self):
        return (self.length*self.breadth)


circle = Circle(5)
square = Square(5)
rectangle = Rectangle(5, 10)

print("Area of Circle : ", circle.area())
print("Area of Square : ", square.area())
print("Area of Rectangle : ", rectangle.area())

#Ques 2:
class Travel:
    def _init_(self, passengerCount, distance, mode):
        self.__no_of_passengers = passengerCount
        self.travel_distance = distance
        self.mode_of_transportation = mode

    def getNoOfPassengers(self):
        return self.__no_of_passengers

class Bus(Travel):
    def _init_(self, passengers, distance):
        super()._init_(passengers, distance, "Bus")

    def cost_of_trip(self):
        return f"The Cost of Travelling from Dharwad to Belagavi via {self.mode_of_transportation} for {self.getNoOfPassengers()} Passengers is {self.getNoOfPassengers()*100}"

class Train(Travel):
    def _init_(self, passengers, distance):
        super()._init_(passengers, distance, "Train")

    def cost_of_trip(self):
        return f"The Cost of Travelling from Dharwad to Belagavi via {self.mode_of_transportation} for {self.getNoOfPassengers()} Passengers is {self.getNoOfPassengers()*60}"

bus = Bus(11, 120)
train = Train(11, 120)

print(bus.cost_of_trip())
print(train.cost_of_trip())

#Ques 3:
class Car:
    def _init_(self, modelNo):
        self.modelNumber = modelNo

c1 = Car('XYZ123')
c2 = Car('ABC987')

print(f"C1 Model Number {c1.modelNumber} and C2 Model Number {c2.modelNumber}  (Before Swap)")
c1.modelNumber, c2.modelNumber = c2.modelNumber, c1.modelNumber
print(f"C1 Model Number {c1.modelNumber} and C2 Model Number {c2.modelNumber}  (After Swap)")

