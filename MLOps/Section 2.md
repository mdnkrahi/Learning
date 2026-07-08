# Section 2 


**1. Linear Regression kaise kaam karta hai**

Linear Regression ek simple line khichta hai jo do cheezon ke beech ka connection dikhata hai. Jaise main tumhe kehti hoon – jitne ghante tum padhte ho, utne marks aate hain. Main data dekh kar ek line khichti hoon aur kehti hoon “agar tum 3 ghante padhoge to lagbhag 75 marks aa sakte hain”.  

Ye line past examples dekh kar banati hai. Assumptions hote hain jaise line seedhi honi chahiye aur data mein bahut zyada uljhan nahi honi chahiye.

**2. Logistic Regression kya hai aur Linear Regression se kaise alag hai**

Logistic Regression bhi line khichta hai lekin ye line sirf numbers nahi, “haan ya na” ka jawab deta hai. Jaise main tumse poochhti hoon “ye phal seb hai ya nahi?”. Jawab sirf seb ya seb-nahi hota hai.  

Linear Regression number batata hai (jaise weight), Logistic Regression category batata hai (jaise seb hai ya nahi). Dono line khichte hain lekin kaam alag hai.

**3. Decision Tree algorithm kya hai**

Decision Tree ek ped jaisa hota hai jisme main haan-na ke sawal poochhti hoon. Jaise main tumse kehti hoon:  
“Phal gol hai?” → Haan → “Rang laal hai?” → Haan → “To ye seb hai!”  

Har sawal ek branch banata hai. Agar ped bahut bada ho jaaye to woh training data ko zyada yaad kar leta hai (overfitting). Isliye hum ped ko chhota rakhte hain ya branches kaat dete hain.

**4. Random Forest kaise kaam karta hai**

Random Forest matlab bahut saare chhote-chhote Decision Trees ek saath kaam karte hain. Jaise main 10 alag-alag ped bana leti hoon, har ped thoda alag data dekh kar banata hai. Phir sab ped vote karte hain – zyada ped jo kehte hain wahi final jawab hota hai.  

Isliye ye akela ped se behtar hota hai aur galti kam karta hai.

**5. Gradient Boosting kya hai**

Gradient Boosting mein hum ek chhota sa ped banate hain, phir dekhte hain ki kahan galti hui. Us galti ko theek karne ke liye dusra chhota ped banate hain. Phir teesra, chautha… dheere-dheere galtiyan kam hoti jaati hain.  

Jaise main tumhara homework check karti hoon, galtiyan batati hoon, tum sudharte ho, phir main phir check karti hoon. XGBoost, LightGBM, CatBoost isi tarah ke tezi se kaam karne wale tareeke hain.

**6. k-Nearest Neighbors (kNN) kya hai**

kNN matlab “k sabse paas wale dost”. Jaise main tumhe ek naya phal dikhati hoon aur kehti hoon “dekho tumhare paas ke 5 phalon mein se zyada tar seb hain to ye bhi seb hoga”.  

Hum count karte hain ki paas ke kitne examples kis category ke hain. “k” ka matlab hai kitne paas wale dost dekhna hai. Agar k=3 hai to 3 sabse paas wale dekh kar decide karte hain.

**7. Support Vector Machine (SVM) kya hai**

SVM ek line (ya curve) khichta hai jo do groups ko alag-alag rakhta hai. Jaise main seb aur kela ko ek line se alag kar deti hoon taaki dono taraf se sabse zyada doori ho.  

Kernel trick ka matlab hai ki jab line se alag nahi ho paate to hum data ko higher dimension mein le jaate hain jaise ek jadoo se, phir line se alag kar dete hain.

**8. Naive Bayes classifier kab use karte hain**

Naive Bayes ek simple tareeka hai jo har cheez ki alag-alag probability nikaal kar final faisla karta hai. Jaise main kehti hoon “agar rang laal hai aur gol hai to seb hone ki sambhavna zyada hai”.  

Ye tab achha kaam karta hai jab data bahut saara ho aur har feature ek dusre se independent ho (jaise spam mail detect karne mein).

**9. Ensemble methods kya hain aur Bagging aur Boosting mein farak**

Ensemble matlab kai chhote models ko ek saath jod kar ek bada strong model banana. Jaise kai chhote ped milkar ek jungle banate hain.  

Bagging: Kai alag-alag trees banate hain aur unke vote se faisla lete hain (jaise Random Forest).  
Boosting: Ek tree ki galti ko dusra tree theek karta hai, phir teesra uski galti theek karta hai (jaise Gradient Boosting). Dono group banate hain lekin galti theek karne ka tareeka alag hai.

**10. Imbalanced dataset ko kaise handle karte hain**

Beta, soch lo tumhare paas ek box mein 90 seb aur sirf 10 aam hain. Agar model sirf seb dekh kar seekhega to aam aane par galat bata dega.  

Isliye hum:  
- Kam wali cheez (aam) ko zyada baar dikhate hain (oversampling)  
- Ya zyada wali cheez (seb) ko kam kar dete hain (undersampling)  
- Ya model ko bata dete hain ki aam ko galat pehchanna badi galti hai  

Isse model dono cheezon ko achhe se seekh paata hai.

---
