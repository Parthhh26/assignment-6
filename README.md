# **Duck Strategy Pattern Implementation**

##  Overview
This project demonstrates the **Strategy Design Pattern** using a **Duck Behavior Simulation** in Java. The Strategy Pattern allows dynamic behavior changes at runtime by encapsulating behaviors into separate classes.

##  Features
- Implements **encapsulated behaviors** for flying, quacking, and swimming.
- **Dynamically changeable behaviors** using setter methods.
- **Multiple duck types**, each exhibiting different behaviors.
- **Adheres to SOLID principles**, making the system extensible.

---

##  Project Structure
```
.
├── Duck.java
├── FlyBehavior.java
├── QuackBehavior.java
├── SwimBehavior.java
├── FlyWithWings.java
├── FlyNoWay.java
├── Quack.java
├── Squeak.java
├── MuteQuack.java
├── Swim.java
├── Float.java
├── Drown.java
├── MallardDuck.java
├── RedheadDuck.java
├── RubberDuck.java
├── DecoyDuck.java
└── Main.java
```


---

## ** Class Breakdown**

### **[`Duck.java`](Duck.java)**
This is an **abstract base class** for all ducks.

####  Functionalities:
- Contains references to `FlyBehavior`, `QuackBehavior`, and `SwimBehavior`.
- Provides methods to perform actions:
  - `performFly()` - Executes the current fly behavior.
  - `performQuack()` - Executes the current quack behavior.
  - `performSwim()` - Executes the current swim behavior.
- Includes setter methods:
  - `setFlyBehavior(FlyBehavior fb)`
  - `setQuackBehavior(QuackBehavior qb)`
  - `setSwimBehavior(SwimBehavior sb)`
- Abstract method `display()` to be implemented by subclasses.

---

### **Behavior Interfaces**

#### **[`FlyBehavior.java`](FlyBehavior.java)**
Defines the `fly()` method for flying behavior.

#### **[`QuackBehavior.java`](QuackBehavior.java)**
Defines the `quack()` method for quacking behavior.

#### **[`SwimBehavior.java`](SwimBehavior.java)**
Defines the `swim()` method for swimming behavior.

---

### **Concrete Behavior Implementations**

#### **Fly Behaviors**
- **[`FlyWithWings.java`](FlyWithWings.java)** - Implements `fly()` → _"Flying with wings!"_
- **[`FlyNoWay.java`](FlyNoWay.java)** - Implements `fly()` → _"Can't fly!"_

#### **Quack Behaviors**
- **[`Quack.java`](Quack.java)** - Implements `quack()` → _"Quack Quack!!"_
- **[`Squeak.java`](Squeak.java)** - Implements `quack()` → _"Squeak Squeak!!"_
- **[`MuteQuack.java`](MuteQuack.java)** - Implements `quack()` → _"Silent duck!"_

#### **Swim Behaviors**
- **[`Swim.java`](Swim.java)** - Implements `swim()` → _"Swimming normally!"_
- **[`Float.java`](Float.java)** - Implements `swim()` → _"I remain Floating..."_
- **[`Drown.java`](Drown.java)** - Implements `swim()` → _"Sinking in water!"_

---

### **Concrete Duck Classes**

#### **[`MallardDuck.java`](MallardDuck.java)**
Represents a **Mallard Duck**, extending `Duck`.

 Functionalities:
- Uses `FlyWithWings`, `Quack`, and `Swim` behaviors.
- Implements `display()` → _"I am Mallard Duck"_

---

#### **[`RedheadDuck.java`](RedheadDuck.java)**
Represents a **Redhead Duck**, extending `Duck`.

Functionalities:
- Uses `FlyWithWings`, `Quack`, and `Swim` behaviors.
- Implements `display()` → _"I am Redhead Duck"_

---

#### **[`RubberDuck.java`](RubberDuck.java)**
Represents a **Rubber Duck**, extending `Duck`.

 Functionalities:
- Uses `FlyNoWay`, `Squeak`, and `Float` behaviors.
- Implements `display()` → _"I'm a Rubber Duck"_

---

#### **[`DecoyDuck.java`](DecoyDuck.java)**
Represents a **Decoy Duck**, extending `Duck`.

 Functionalities:
- Uses `FlyNoWay`, `MuteQuack`, and `Drown` behaviors.
- Implements `display()` → _"I am a Decoy Duck"_

---

##  UML Class Diagram

![UML Diagram](./UML%20Diagram.png)

---

