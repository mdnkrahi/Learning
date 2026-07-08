# Section 5


## **1. Batch, Mini-batch aur Stochastic Gradient Descent mein farak**

Gradient Descent ka matlab hai galti ko kam karne ke liye chhote-chhote steps lena.  

- **Batch**: Poora data ek saath dekh kar step lena. Jaise tum poora homework ek baar mein karte ho.  
- **Mini-batch**: Data ko chhote groups mein baant kar step lena. Jaise tum 10-10 sawal karke check karte ho.  
- **Stochastic**: Har ek example dekh kar step lena. Jaise har sawal ke baad turant check karna.  

Mini-batch sabse common hai kyunki ye tezi se aur achhe se kaam karta hai.



---


## **2. Optimization Algorithms jaise SGD, Momentum, Adam, RMSprop**

SGD sirf chhote steps leta hai. Momentum matlab pehle wali speed ko yaad rakhna – jaise cycle chalate waqt downhill jaane par tez ho jaate ho.  

Adam aur RMSprop smart tareeke hain jo har step ka size khud decide karte hain. Jaise tum chalte waqt dekhte ho ki rasta smooth hai ya gadha, uske hisaab se kadam badalte ho. Ye tezi se aur sahi direction mein le jaate hain.




---


## **3. Learning Rate Scheduling kya hai**

Learning rate matlab kitna bada step tum lete ho. Agar shuru mein bada step lo to jaldi pahunch jaoge, lekin end mein chhote steps lo warna galat jagah pahunch jaoge.  

Scheduling ka matlab hai time ke saath learning rate ko chhota karte jaana. Jaise pehle tez daudte ho, phir dheere chalte ho taaki sahi jagah ruk sako.




---


## **4. Hyperparameter Tuning ke tareeke**

Hyperparameters wo cheezein hain jo hum pehle se decide karte hain jaise kitne groups, kitna bada step, kitne layers.  

- **Grid Search**: Har possible combination try karna (jaise har size aur har color try karna).  
- **Random Search**: Random combinations try karna – ye jaldi achha result de sakta hai.  
- **Bayesian Optimization**: Smart tareeka jo pehle wale results dekh kar agla best combination choose karta hai.




---


## **5. Early Stopping kya hai**

Early Stopping matlab training ko time par rok dena. Jaise tum practice test dete ho. Jab practice test ke marks badhne ki jagah girne lagte hain to tum ruk jaate ho.  

Ye overfitting rokta hai. Model training data ko zyada yaad karne lagta hai isliye hum ruk jaate hain jab naye data par performance girne lage.

Yahan ek simple code demo hai jo early stopping ka idea dikhata hai:

```python
loss_values = [5.0, 3.5, 2.8, 2.5, 2.6, 2.9]  # galti kitni hai har round mein
best_loss = 100
patience = 2   # kitne round tak wait karna hai
wait = 0

for i, loss in enumerate(loss_values):
    if loss < best_loss:
        best_loss = loss
        wait = 0
    else:
        wait = wait + 1
    if wait >= patience:
        print("Training ruk gaya round", i)
        break
```

Ye code dekhta hai ki galti badh rahi hai ya nahi. Agar badhe to ruk jaata hai.




---


## **6. Dropout, Batch Normalization aur Layer Normalization**

Dropout: Training ke dauran kuchh cells ko randomly band kar dena. Jaise tum padhte waqt kabhi-kabhi aankh band kar ke yaad karte ho. Isse model strong banta hai.  

Batch Normalization: Har group (batch) ke data ko theek se arrange karna taaki training tez aur stable ho. Jaise har test se pehle tum apne answers ko sahi format mein laate ho.  

Layer Normalization: Poori layer ke data ko theek karna. Ye bhi training ko behtar banata hai.




---


## **7. Weight Initialization Techniques**

Weight initialization matlab shuru mein har cell ko kitna weight dena. Agar sab weights zero kar doge to network kuchh nahi seekhega.  

Achha tareeka ye hai ki weights ko chhote random numbers se shuru karo taaki signal aage-piche achhe se ja sake. Jaise tum nayi cycle chalana shuru karte ho to pehle dheere dheere balance seekhte ho.




---


## **8. Vanishing aur Exploding Gradients**

Vanishing Gradient: Signal itna kamzor ho jaata hai ki peeche tak pahunchta hi nahi. Jaise tum door se kisi ko awaaz dete ho aur woh sun nahi paata.  

Exploding Gradient: Signal itna tez ho jaata hai ki sab kuchh bigad jaata hai. Jaise cycle tez downhill jaate waqt control kho dena.  

Inko theek karne ke liye hum special tareeke use karte hain jaise better activation functions ya normalization.




---


## **9. Learning Rate Finder aur One-Cycle Policy**

Learning Rate Finder ek tareeka hai jisse hum dekhte hain ki sabse achha learning rate kya hai. Jaise tum alag-alag speed se daud kar dekhte ho ki kaunsi speed sabse comfortable hai.  

One-Cycle Policy mein hum pehle learning rate badhate hain phir dheere kam karte hain. Ye training ko tezi se aur achhe se complete karta hai.




---


## **10. Mixed Precision Training kya hai**

Mixed Precision Training mein hum kuchh calculations chhote numbers (float16) mein karte hain aur kuchh bade numbers (float32) mein. Jaise tum ghar ka hisaab chhote copy mein aur bada hisaab bade register mein rakhte ho.  

Faayda: Training tez hoti hai, kam memory lagti hai aur badi machine par bhi kaam aasani se ho jaata hai.


---
