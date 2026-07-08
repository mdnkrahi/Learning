# Section 3 

## **1. Clustering kya hai aur K-Means algorithm kaise kaam karta hai**

clustering ka matlab hai cheezon ko groups mein baantna bina kisi ko naam bataye. Jaise main tumhe ek bada dibba deti hoon jisme seb, kela, santre, aam pade hain. Tum khud dekho aur 3 groups bana do – gol wale ek taraf, lambe wale dusri taraf.  

K-Means mein hum pehle 3 centers (jaise 3 bowl) rakh dete hain. Phir har phal ko sabse paas wale bowl mein daal dete hain. Phir bowl ko phalon ke beech le jaate hain. Ye baar-baar karte hain jab tak groups achhe na ban jaayein. Limitation ye hai ki pehle se hi batana padta hai kitne groups chahiye aur groups gol hi bante hain.



---


## **2. Hierarchical Clustering kya hai**

Hierarchical clustering ek family tree jaisa banata hai. Pehle har phal apna alag group hota hai. Phir do sabse paas wale groups ko jod dete hain. Phir phir jodte hain. Aakhir mein ek bada tree ban jaata hai.  

Do tarike hain – ek neeche se shuru karke upar jodte hain (agglomerative), dusra upar se shuru karke neeche todte hain (divisive). Jaise tum apne rishtedaaron ka family tree bana rahe ho.



---


## **3. DBSCAN kya hai**

DBSCAN groups banata hai jahaan phal ek dusre ke paas-paas hote hain. Agar koi phal akela hai aur kisi group ke paas nahi to usse “noise” (ganda data) maante hain.  

Isme hum pehle se groups ki sankhya nahi batate. Ye groups ko kisi bhi shape ka bana sakta hai – gol, lamba, tedha – jo K-Means nahi kar paata. Aur akela phal ko alag kar deta hai.



---


## **4. Principal Component Analysis (PCA) kya hai**

PCA data ko chhota karne ka tareeka hai. Jab tumhare paas bahut saare measurements hote hain (jaise har phal ke liye rang, size, weight, sweetness, 10 cheezein) to hum unme se sabse important 2-3 cheezein nikaal lete hain.  

Jaise tum ek 3D khilone ki sirf shadow dekh kar uske baare mein samajh jaate ho. PCA bhi aisa hi karta hai – data ko 2D ya 3D mein laa deta hai taaki hum dekh sakein.



---


## **5. t-SNE kya hai aur PCA se kaise alag hai**

t-SNE bhi data ko chhota karta hai lekin iska kaam hai groups ko paper par sundar tarike se alag-alag dikhaana. Jaise tum school ke bachchon ko groups mein baithate ho taaki dost ek saath baithen.  

PCA line khichta hai aur important cheezein rakhta hai. t-SNE groups ko achhe se alag dikhane ki koshish karta hai. Isliye groups dekhne ke liye t-SNE behtar hota hai.



---


## **6. Autoencoders kya hain**

Autoencoder ek machine hai jo input ko copy karna seekhti hai lekin beech mein ek chhota sa rasta hota hai. Jaise tum ek photo ko chhote size mein compress karte ho phir wapas bada karte ho.  

Beech ka chhota rasta important cheezein hi yaad rakhta hai. Isliye ye unsupervised learning mein useful hai – jaise galat photo ko pehchanna ya important features nikaalna.



---


## **7. Semi-supervised learning kya hai**

Semi-supervised learning mein hume kuchh examples ke saath naam (label) diye hote hain aur bahut saare bina naam ke. Jaise main tumhe 10 seb aur 10 kela ke naam bataati hoon aur phir 100 aur phal bina naam ke deti hoon.  

Tum thode naam wale examples se seekh kar baaki phalon ko groups mein daal sakte ho. Ye supervised aur unsupervised dono ka mix hai.



---


## **8. Anomaly detection kya hai**

Anomaly detection ka matlab hai wo cheez dhundna jo group mein nahi fit hoti. Jaise tumhare saare phal seb aur kela ke groups mein hain lekin ek phal bilkul alag hai – na gol, na lamba, rang bhi alag. Wo anomaly hai.  

Ye unsupervised tareeke se groups bana kar dhundta hai ki kaun sa phal kisi group mein nahi aa raha.



---


## **9. Clustering algorithms ko kaise evaluate karte hain**

Clustering ko evaluate karne ke liye hum dekhte hain ki groups kitne alag-alag hain. Jaise tum dekhte ho ki ek group ke phal sab laal-gol hain aur dusre group ke sab lambe-peele hain.  

Agar groups ke andar sab ek jaise hain aur groups ek dusre se alag hain to clustering achha maana jaata hai. Hum numbers nikaalte hain jaise groups kitne tight hain.


---


## **10. Association Rule Learning kya hai**

Association rule ka matlab hai rules dhundna jaise “agar koi seb aur kela kharidta hai to aksar aam bhi kharidta hai”. Jaise dukaan wale dekhte hain ki log aksar ye teen cheezein saath mein lete hain.  

Algorithms jaise Apriori aur FP-Growth aise rules nikaalte hain. Ye market mein cheezon ko saath rakhne mein madad karta hai.

---
