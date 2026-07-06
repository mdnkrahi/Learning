# Python

## step 1


Socho Python ek **khel ka khilona** hai. Jaise school mein hum games khelte hain, waise hi computer ko game sikhane ke liye yeh sab basic cheezein chahiye. Main har cheez ko story aur example se samjhaunga.

### 1. **Variables** (Jaise dabbe ya khazana)
- Variable matlab **naam wala dabba** jismein hum cheezein rakh sakte hain.
- Jaise tumhara school bag hai – usme tum books, pencil, tiffin rakh sakte ho. Bag ka naam "school-bag" hai.
- Computer mein bhi: `a = 5`  →  Yeh matlab "a" naam ka dabba banaya aur usme number 5 rakh diya.
- Baad mein tum us dabbe se 5 nikaal sakte ho ya nayi cheez daal sakte ho.

**Simple example**:  
Tumhara naam = "Nadeem"  
Tumhari age = 33  
Yeh dono variables hain.

### 2. **Data Types** (Dabba mein kya rakha hai?)
- Har dabbe (variable) mein alag-alag cheez rakh sakte ho. Computer ko pata hona chahiye ki kis tarah ki cheez hai.
- **Numbers (int, float)**: Jaise 5, 10, 3.5 (poore number ya decimal wale).
- **Words (string)**: "Hello", "Apple", "Mera naam Nadeem hai" → yeh sab text hain.
- **True/False (bool)**: Jaise kya school band hai? → True (haan) ya False (nahi).

**Bachchon wala example**:  
Tumhara school bag mein ho sakta hai – pencil (text), 5 notebooks (number), ya kya aaj holiday hai? (True/False).

### 3. **Operators** (Jaise khelne ke tools)
- Yeh woh cheezein hain jo numbers ya words pe kaam karti hain.
- **+ - * /** : Jaise 2 + 3 = 5 (jaise doodh mein cheeni milana)
- **==** : Kya yeh barabar hai? (5 == 5 → True)
- **> <** : Kya yeh bada hai? (10 > 5 → True)

**Example**:  
Tumhare paas 10 toffee hain. Dost ke paas 4.  
Operator use karke dekh sakte ho: 10 > 4 → Haan, tumhare paas zyada hain!

### 4. **Conditionals** (Agar-agar wala khel)
- Yeh **decision lene** wala hissa hai. Jaise mummy kehte hain "Agar tum homework kar loge to ice-cream milegi".
- Python mein: **if**, **elif**, **else**

**Story example**:  
Agar barish ho rahi hai (condition true) → ghar mein ruko aur game khelo.  
Nahi to (else) → bahar khelo.

Code jaisa socho:  
```python
if aaj_barish_hai == True:
    ghar_mein_khelo()
else:
    bahar_khelo()
```

### 5. **Loops** (Baar-baar repeat karna)
- Jab ek kaam ko kai baar karna ho, tab loop use karte hain.
- **For loop**: Jaise class mein 10 students hain – har student ka naam padhna hai (10 baar repeat).
- **While loop**: Jab tak mummy na bulaaye, khelte raho.

**Bachchon wala example**:  
Tumhe 5 baar "I love Python" likhna hai. Loop se sirf ek line likhoge aur woh 5 baar repeat ho jayega. Bahut mehnat bach jaati hai!

### 6. **Functions** (Jaise mummy ka special recipe)
- Function matlab **ek chhota machine** jo kaam karta hai jab tum usko bulao.
- Jaise mummy ko bolo "Mummy, chai bana do" → woh recipe follow karke chai bana deti hain.
- Tum bhi function bana sakte ho: `def chai_banao()` → andar recipe likho.

**Example**:  
Ek function banao jo do numbers ko jod de. Baar-baar use kar sakte ho bina nayi nayi line likhe.

---

**Summary**:  
Yeh sab cheezein Python ko **zinda** banati hain. Jaise ghar banane ke liye pehle bricks (variables), phir cement (operators), phir plan (conditionals & loops), aur phir ready rooms (functions) chahiye.

#
#
#
#

## step 2





Pehle humne basic tools (variables, loops etc.) seekhe the. Ab yeh **dabbey aur almariyan** hain jismein hum cheezein saaf-safai se rakh sakte hain. Jaise school bag, tiffin box, pencil box – har ek ka apna kaam hai.

### 1. **Lists** (Jaise ek lambi shopping list ya train ki bogi)
- List ek **line mein cheezon ka group** hai jo order mein rehti hai.
- Isme same cheez kai baar aa sakti hai.
- Hum isme nayi cheez daal sakte hain, nikaal sakte hain, badal sakte hain (jaise bag mein cheezein daalte-rehte ho).

**Bachchon wala example**:  
Tumhari favourite fruits ki list:  
`["Apple", "Banana", "Mango", "Apple"]`  
Pehla number 1 hai (Apple), dusra Banana. Tum 3rd position pe kuch bhi badal sakte ho. Jaise school mein roll number list.

**Khel**: List ko badal sakte ho – ek fruit nikaalo, doosra daalo.

### 2. **Tuples** (Jaise sealed tiffin box)
- Tuple bhi list jaisa hai – cheezon ka group, order mein.
- Lekin **bandh diya gaya hai** – ek baar banane ke baad kuch badal nahi sakte.
- Safe aur strong hota hai jab tumhe cheezein badalni nahi chahiye.

**Example**:  
Tumhara school address:  
`("Raipur", "Chhattisgarh", "India")`  
Yeh change nahi kar sakte kyunki address fixed hota hai. Jaise birthday date – woh kabhi nahi badalti.

**Khel**: Ek baar banaya, phir lock kar diya. Koi change nahi!

### 3. **Sets** (Jaise magic bag jismein duplicate nahi rehte)
- Set mein sirf **unique cheezein** (alag-alag) rakh sakte ho. Koi cheez do baar nahi aa sakti.
- Order matter nahi karta (jaise bag mein sab ek saath gire hue).
- Bahut tez check karta hai – kya yeh cheez andar hai?

**Example**:  
Tumhare class ke unique dost:  
`{"Rahul", "Priya", "Aman"}`  
Agar "Rahul" do baar daaloge to bhi ek hi rahega. Duplicate hat jaata hai jaise jaadu!

**Khel**: School canteen mein alag-alag flavours ka set – koi repeat nahi.

### 4. **Dictionaries** (Jaise school ka attendance register ya treasure map)
- Dictionary mein har cheez ka **naam (key) aur uski value** hoti hai.
- Jaise dictionary mein word aur uska matlab.
- Bahut tez dhund sakte ho – naam bolo, cheez mil jaati hai.

**Bachchon wala example**:  
Tumhara favourite games ka register:  
```python
{
  "Cricket": "Bat aur ball se khelte hain",
  "Football": "Goal maarna hai",
  "Ludo": "Ghar tak pahunchna hai"
}
```
"Cricket" naam bolo → turant uski value (matlab) mil jaayegi.

**Khel**: Jaise mummy fridge pe note chipkaati hain – har cheez ka naam aur kya hai.

---

**Summary**:  
- **List** → Badalne wali lambi line (shopping list)  
- **Tuple** → Locked aur safe box (birthday date)  
- **Set** → Magic bag jismein sab unique (no duplicates)  
- **Dictionary** → Smart register jismein naam se cheez mil jaati hai  

 
 #
#
#
#
 ## step 3
 
 
 
 
 ## **“Object Oriented Programming”** 
 – jaise ek poora **khel ka sheher** banana. Pehle wali cheezein (variables, lists) chhote tools the. Ab hum bade-bade **khelne wale characters aur unke ghar** bana rahe hain.

### 1. **Classes** (Jaise blueprint ya recipe)
- Class ek **naksha** ya **design** hai. Asal cheez nahi, sirf plan.
- Jaise car ka naksha – dikhaata hai car kaisi dikhegi, kitne wheels, engine kaisa.

**Example**:  
`class Car:` → Yeh sirf design hai. Abhi koi asli car nahi bani.

**Bachchon wali story**: Mummy ke paas cake ka recipe (class) hai. Recipe se kai cakes bana sakte ho.

### 2. **Objects** (Asli cheez jo recipe se banti hai)
- Object class se banaya hua **asli khel ka samaan** hai.
- Ek class se kai objects bana sakte ho.

**Example**:  
`my_car = Car()` → Ab yeh asli red wali car ban gayi jo sach mein chal sakti hai.

**Simple**: Class = Cake ka recipe. Object = Asli cake jo tum kha sakte ho. Ek recipe se 10 cakes (objects) bana sakte ho.

### 3. **Inheritance** (Jaise beta papa se features leta hai)
- Nayi class purani class se sab kuch **virasat** mein le sakti hai aur thoda apna bhi jod sakti hai.
- Bachchon ko mummy-papa ke features milte hain (tall, smart) aur kuch naya bhi.

**Example**:  
`class Bike(Car):` → Bike car ki saari cheezein le legi (wheels, engine) aur apne hisaab se fast bana legi.

**Story**: Papa ka cycle ka design hai. Beta usi se naya racing bike banaata hai – purana design + apna speed.

### 4. **Encapsulation** (Jaise secret dabba ya tiffin)
- Apni important cheezein ** andar chhupa** lena. Bahar wale sirf bahar se use kar sakein, andar ka sab kuch na dekh sakein.
- Jaise tiffin mein mummy ne sabzi daali hai – tum sirf khol ke kha sakte ho, andar kaise banaya woh nahi dekh sakte.

**Example**: Car mein engine chhupa hota hai. Tum sirf steering aur accelerator chhute ho, engine khud nahi chhedte.

Yeh safety ke liye hota hai.

### 5. **Polymorphism** (Ek naam, alag-alag kaam)
- Ek hi naam ka button alag-alag cheezon ke saath alag-alag kaam kare.
- Jaise “bol” button:  
  - Dog ko bolo → “Bhow Bhow”  
  - Cat ko bolo → “Meow”  
  - Bird ko bolo → “Chir Chir”

**Example**: Ek function `sound()` sab animals mein hai, lekin har animal apni awaaz nikalta hai.

**Khel**: Sab “dance” karo bolo – tum alag tarike se dance karoge, teacher alag, dost alag!

### 6. **Abstraction** (Sirf important button dikhaana)
- Andar ka complicated kaam chhupa ke sirf **simple button** dikhaana.
- Jaise TV remote – andar bahut wires aur circuit hain, lekin tumhe sirf Power aur Volume button chahiye.

**Example**: Car chalate waqt tumhe engine ka pura science nahi pata hona chahiye. Sirf “start” button aur drive karo.

---

**Summary**:

- **Class** = Cake ka recipe (naksha)  
- **Object** = Asli cake (jo ban gaya)  
- **Inheritance** = Papa se features lena aur apna jodna  
- **Encapsulation** = Secret tiffin – andar mat dekho  
- **Polymorphism** = Ek naam, kai alag-alag tricks  
- **Abstraction** = Sirf remote ke button dikhao, andar ka jadoo chhupao  

Yeh sab milkar bada-bada program banate hain jaise ek poora video game jismein cars, bikes, animals sab apne roles mein khel rahe hain.









#
#
#
##
#
#
##
#
#
##
#
#
##
#
#
##
#
#
##
#
#
##
#
#
##
#
#
#
