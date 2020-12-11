## Assignment 6 (Group-1)(Week-5)

> Program Assignment (15-points)

## Grading Program 2

User က အမှတ်တွေ သိမ်းပါလိမ့်မယ်။ သူသိမ်းချင်သလောက်ကို သိမ်းမှာဖြစ်ပါတယ်။ တကယ်လို့ ပြန်ပြီးထုတ်ကြည့်ချင်တဲ့ အခါမှာ A ရသူ ဘယ်နှယောက် B ကတော့ ဘယ်နှယောက် စသည်ဖြင့် ထုတ်ပြပေးရမှာဖြစ်ပါတယ်။

**(Group ထဲမှာတင်ထားတဲ့ ToDoList Program နဲ့ သဘောတရားတူပါမယ်)**

### Step-1

Infinite Loop တစ်ခုရှိပါမယ်။ Loop ပတ်တိုင်းမှာ input တစ်ခုအမြဲတောင်းပါမယ်။

* E = exit (ဘာ Output မှ မထုတ်ပဲ Program(Loop) က ထွက်မယ်)
* A = append (အသစ်ထည့်မယ်)
* P = print (output ထုတ်ပေးမယ်)

အပေါ်က သုံးခုလုံးတစ်ခုမှ မဟုတ်ရင် invalid input ဆိုပြီး ထုတ်ပေးရပါမယ်

***(Sample Input & Output ကို သေချာကြည့်ပေးပါ)***

### Step-2 (A = append)

user က A လို့ ရိုက်လိုက်တဲ့ အခါမှာ integer input(အမှတ်) တောင်းရပါမယ်။ ပြီးရင် အဲ့ဒီ အမှတ်ကို သိမ်းထားရပါမယ်။

### Step-3 (P = print)

user က P လို့ ရိုက်လိုက်တဲ့ အခါမှာ output ထုတ်ပေးရပါမယ်။

ထုတ်ရမယ့် Output က user ထည့်ခဲ့တဲ့ အမှတ်တွေထဲကမှ

Grade-A ဘယ်နှယောက်ရကြောင်း

Grade-B ဘယ်နှယောက်ရကြောင်း

စသည်ဖြင့် Grade-E အထိ ဘယ်နှယောက်ရကြောင်းကို ထုတ်ပေးရပါမယ်

Invalid အမှတ် ထည့်မိသူ ဘယ်နှယောက်ရှိလဲ ဆိုတာပါ ထုတ်ပေးရပါမယ်။

*Example*
```
Grade-A: 4
Grade-B: 5
Grade-C: 10
Grade-D: 2
Grade-E: 0
Invalid: 1
```

**ဖြစ်ရမည့် အမှတ်နဲ့ အဆင့်များ** (Assignment 4 နဲ့တူပါတယ်)

| Number or Mark | Grade |
| --- | --- |
| 0 to 19 | E |
| 20 to 39 | D |
| 40 to 59 | C |
| 60 to 79 | B |
| 80 to 100 | A |
| others | invalid |

### Step-4 (E = exit)

user က E လို့ ရိုက်လိုက်မယ်ဆိုရင် Loop ကနေ Break ပေးရပါမယ်။

(Program ရပ်ပေးရပါမယ်)

***တခြား output အပိုများ ထည့်မပေးရပါ။***

##### Sample Input & Output 1
```
Enter (A,P,E): A
Enter mark: 90
Enter (A,P,E): A
Enter mark: 99
Enter (A,P,E): A
Enter mark: 77
Enter (A,P,E): P
Grade-A: 2
Grade-B: 1
Grade-C: 0
Grade-D: 0
Grade-E: 0
Invalid: 0
Enter (A,P,E): A
Enter mark: -2 
Enter (A,P,E): P
Grade-A: 2
Grade-B: 1
Grade-C: 0
Grade-D: 0
Grade-E: 0
Invalid: 1
Enter (A,P,E): E
```

<br>
<hr>

***အောက်ဖော်ပြပါ အချက်လက်များမပြည့်စုံပါက အမှတ်ရရှိမည်မဟုတ်ပါ***

* file name ကို ထုံးစံအတိုင်း email နဲ့ ထုတ်ပေးရပါမယ် (အောက်ဆုံးမှာ ထည့်ရမယ့် format ရှိပါတယ်)
* တောင်းရမယ့် input တွေမှာ Sample input အတိုင်းဖြစ်ရပါမယ်
* Enter (A,P,E): 
* Enter mark: 
* Grade-A: (number)
* Invalid: (number)
  

* Program ကို စိတ်ကြိုက် ရေးနိုင်ပါတယ်။ (output ကိုသာ ကန့်သတ်ထားတာပါ)
* infinite loop or မှားယွင်းတဲ့ loop ဖြစ်နေပါက အမှတ်လုံးဝမရပါ
* Program နဲ့ စာစစ်တာဖြစ်တဲ့အတွက် output ကို Sample ပြထားသလိုပဲ ထုတ်ပေးပါခင်ဗျ။ Output အပိုထည့်တဲ့အခါ အမှတ်မရပဲ ဖြစ်တတ်ပါတယ်

**File ကို save တဲ့ အခါမှာ file name ကို အောက်ပါ Format အတိုင်း ပေးကြဖို့ အရေးကြီးပါတယ်။**

> ```asm6_(မိမိemailရှေ့ကနာမည်).py```

> *သင့်ရဲ့ email သည် ```mgmg123@gmail.com``` ဆိုပါစို့*

> ```asm6_mgmg123.py``` ဟု ပေးရမည်

> email မှာ ```'.'```(dot) တွေပါနေပါက ဖြုတ်ပြီးထည့်ပေးပါ

> ဥပမာ- email က ```kyaw.gyi.1500@gmail.com``` ဆိုရင်

> ```asm6_kyawgyi1500.py``` လို့ရေးရပါမယ်


* ***အထက်ပါအတိုင်း မှန်ကန်အောင်ပေးရမည်***
* **မသေချာလျှင် Page မှာလာပြီး မေးမြန်းပေးပါ**
* **email name/ file name မှားသူများသည် အမှတ် ရမည်မဟုတ်ပါ**

သေချာပြီဆိုလျှင် ဒီ link မှာ Assignment ထပ်ရပါမည်

[https://forms.gle/1RCxWCBKEbDtQyVL6](https://forms.gle/1RCxWCBKEbDtQyVL6)