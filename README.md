## Fashion-MNIST dataseti yordamida kiyimlarni qaysi turkumga tegishli ekanligini bashorat qilish

#### 1. ```Fashion-MNIST``` dataseti haqida qisqacha ma'lumot
```MNIST``` (Modified National Institute of Standards and Technology) ma'lumotlar bazasi turli xil tasvirlarni qayta ishlash tizimlarini o'qitish uchun keng qo'llaniladigan qo'lda yozilgan raqamlarning katta ma'lumotlar bazasidir. Ma'lumotlar bazasi mashinani o'rganish sohasida o'qitish va sinovdan o'tkazish uchun ham keng qo'llaniladi. Ijodkorlar fikricha, NISTning oʻquv maʼlumotlar toʻplami - Amerika aholisini roʻyxatga olish byurosi xodimlaridan, sinov maʼlumotlar toʻplami esa amerikalik oʻrta maktab oʻquvchilaridan olingani uchun u mashinani oʻrganish boʻyicha tajribalar uchun unchalik mos emas edi. Oq-qora tasvirlar 28x28 pikselli matritsalarga joylashtirish uchun normallashtirilgan va kulrang kanal holatida shakllantirilgan.

```Fashion-MNIST``` ma'lumotlar bazasida 60 000 ta o'quv tasvir(```train data```)lari va 10 000 ta sinov tasvir(```test data```)lari mavjud. 

![cmd](https://github.com/MisterFoziljon/Fashion-MNIST/blob/main/rasmlar/digits.jpg)


#### 2. Loyihani yuklab olish uchun quyidagi ketma-ketlikni bajaring:
  * `windows+R` klavishlarini bosing va paydo bo'lgan oynaga `cmd` buyrug'ini yozing OK tugmachasini bosing.
  
  ![cmd](https://github.com/MisterFoziljon/Fashion-MNIST/blob/main/rasmlar/cmd.png)

  * Loyihani quyidagi link yordamida yuklab oling. (Loyiha uchun yaratilgan fayl adresni o'zingiz ko'rsatishingiz mumkin)

        C:\> git clone https://github.com/MisterFoziljon/Fashion-MNIST.git

  * Loyiha joylashgan faylga kiring.
         
        C:\> cd Fashion-MNIST


#### 3. Proyektni ishlatish uchun kerakli modullarni virtual environment yaratib o'rnatib oling.
* O'zingizdagi pip ni so'nggi versiyasiga yangilang.

        C:\Fashion-MNIST> python -m pip install --upgrade pip
        
* virtual environment yaratish uchun virtualenv modulini o'rnating.
        
        C:\Fashion-MNIST> python -m pip install --user virtualenv

* Yangi environment yaratish uchun unga nom bering.
        
        C:\Fashion-MNIST> python -m venv sizning_env
        
* Virtual environmentni ishga tushiring(aktivlashtiring).
        
        C:\Fashion-MNIST> sizning_env\Scripts\activate.bat
        
* Virtual environment ichiga loyiha ishlashi uchun kerakli bo'lgan modullarni o'rnating (requirements.txt faylining ichida barchasi mavjud).
        
        (sizning_env) C:\Fashion-MNIST> pip install -r requirements.txt


#### 4. Proyektni ishlatish uchun jupyter notebook ni ishga tushiring.

        (sizning_env) C:\Fashion-MNIST> jupyter notebook
        
  * ```CNN yordamida model o'qitish.ipynb``` ni ishga tushiring. Usbu notebookda Keras.io saytidagi MNIST datasetini o'qib olish, uni train va test datalariga ajratish, datalarni size va shape larini train uchun moslash hamda normallashtirish ko'rsatilgan. Dataset yordamida Convolutional Neural Network ishlab chiqilgan va u yordamida model train va evaluate qilingan. Model h5 formatda saqlanadi. Ushbu notebookni birinchi bo'lib ishga tushirib ```modelni qayta o'qiting```!!! Chunki model githubga yuklanmadi.
  
  * ```Modelni sinovdan o'tkazish.ipynb``` ni ishga tushiring. Ushbu notebook yordamida saqlangan modelni load qilish va yangi test qilish datalari yordamida bashorat qilish (predict) ko'rsatib o'tilgan.


#### 4. Proyektni streamlit yordamida deploy qilish.

        (sizning_env) C:\Fashion-MNIST> streamlit run streamlit.py

  * Proyekt ```local server```da ishga tushadi va quyidagicha ko'rinishda bo'ladi:


![streamlit1](https://github.com/MisterFoziljon/MNIST/blob/main/rasmlar/streamlit1.png)
  
  * Rasm faylini yuklab oling va ```Predict``` tugmachasini bosing. Model yuklab olingan tasvirni qaysi tukumdagi kiyimga tegishli ekanligini bashorat qiladi. Bundan tashqari softmaxdan chiqqan ehtimollik natijasi ham ekranga chiqadi.


![streamlit3](https://github.com/MisterFoziljon/Fashion-MNIST/blob/main/rasmlar/answer.png)
