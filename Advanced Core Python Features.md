# **Advanced Core Python Features – Code + Bahut Simple Explanation**  

Main har ek cheez ko **line-by-line** samjhaata hoon. Bilkul dheere-dheere.

---

### 1. **Decorators** (Magic Sticker Trick)

**Simple Idea**: Kisi bhi function ke upar ek sticker laga do. Jab bhi woh function chale, pehle sticker ka extra kaam ho jaaye.

```python
# Step 1: Magic sticker banate hain
def magic_sticker(func):          # func = asli kaam
    def new_function():           # Naya wrapper
        print("🌟 Magic shuru! Extra safety check...")   # Extra kaam
        func()                    # Asli function chalao
        print("🌟 Magic khatam! Bahut achha kaam kiya!")
    return new_function           # Sticker wala naya function lauta do

# Step 2: Sticker lagaate hain
@magic_sticker
def hello():
    print("Hello dost! Main Nadeem ka Python program hoon.")

# Step 3: Chalao
hello()
```

**Line-by-Line Samajh**:
- `@magic_sticker` → Yeh sticker hai.
- Jab `hello()` call karte ho, pehle extra messages print hote hain.
- Jaise school bag pe "Super Student" sticker laga do – har baar bag uthaoge to woh khud bolega "Bahut achha!"

---

### 2. **Generators** (Ek-Ek Karke Candy Machine)

**Simple Idea**: Saari cheezein ek saath mat banao. Jab maango tab do. Bahut kam jagah lagti hai.

```python
def candy_machine(max_candies):
    for i in range(max_candies):   # 0 se max_candies-1 tak
        print(f"🍭 Machine mein candy {i} taiyaar kar raha hoon...")
        yield i                    # Ek candy abhi do, baaki rakh lo

# Use karte hain
gen = candy_machine(5)   # Machine ready, lekin abhi kuch nahi diya

print("Pehli candy maangi →", next(gen))
print("Doosri candy maangi →", next(gen))
```

**Line-by-Line Samajh**:
- `yield` jaise bolna "ek candy abhi de raha hoon, baad mein aur maangna".
- Agar 1 lakh candies hon to bhi memory nahi khayega.

---

### 3. **Context Managers** (Automatic Darwaza)

**Simple Idea**: File kholo → kaam karo → khud band ho jaaye. Bhoolne ka chance nahi.

```python
class SafeBox:                     # Apna chhota safe box
    def __enter__(self):           # Darwaza kholo
        print("🔒 Safe khol diya - andar jaao!")
        return "Yeh andar ka khazana hai: Gold coins!"
    
    def __exit__(self, a, b, c):   # Darwaza band karo (chahe error ho)
        print("🔐 Safe band ho gaya - sab safe!")

# Use karte hain
with SafeBox() as khazana:
    print(khazana)                 # Khazana use karo
    # Yahan kuch bhi karo, end mein automatically band hoga
```

**Line-by-Line Samajh**:
- `with` likhte hi `__enter__` chal jaata hai.
- Block khatam hote hi `__exit__` chal jaata hai.
- Jaise fridge kholo, doodh nikalo, band kar do – bhool gaye to bhi band ho jaaye.

---
