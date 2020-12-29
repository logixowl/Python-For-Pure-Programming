## Assignment 9 (Group-1)(Final Week)

> Program Assignment

## Number Converter

### Step-1

number တစ်ခုကို input တောင်းပါ။ (input ထဲမှာ ဘာ output မှ မပြရပါ)
နှစ်သက်ရာ Loop တစ်မျိုးနဲ့ number အတိုင်း loop ပတ်ပါ။

ဥပမာ- number က 5 ဆိုရင် loop 5 ခါအတိအကျ ပတ်ပေးရပါမယ်

### Step-2

Loop အတွင်းမှာ input နှစ်ခါတောင်းရပါမယ်

**ပထမ input**

user ထည့်လိုက်တဲ့ string input ကို ယူပါ။ ပြီးရင် ```split(" ")``` ကို သုံးပြီး value နှစ်ခု ယူပါ

ပထမ value သည် from base ဖြစ်ပြီး ဒုတိယ value သည် to base ဖြစ်ပါတယ်

**Example**

* ```2 10``` ဆိုရင် base2 ဖြစ်တဲ့ binary ကနေ base10 ဖြစ်တဲ့ Decimal value ပြောင်းပေးရမှာပါ
* ```8 16``` ဆိုရင် base8 ဖြစ်တဲ့ octal value ကနေ base16 ဖြစ်တဲ့ hexadecimal value ကို ပြောင်းပေးရမှာဖြစ်ပါတယ်

ဖြစ်ရမယ့် base က ၄ မျိုးပဲ ရှိပါတယ်
```
2 = binary
8 = octal
10 = decimal
16 = hexadecimal
```
**ဒုတိယ input**

နောက် လာမယ့် input က ပြောင်းရမယ့် value ဖြစ်ပါတယ်

> **Hint**: value ကို decimal အရင်ပြောင်းပြီးမှ tobase အတိုင်း ပြန်ပြောင်းသင့်ပါတယ်
> ```bin(), oct(), hex()```

*တကယ်လို့ နားမလည်ဘူးဆိုရင် [Python Numerics](../files/numeric.md) သင်ခန်းစာကို ပြန်ကြည့်ပါ*

> ပြောင်းလို့ ရလာတဲ့ Value ကို output ထုတ်ပြပါ

***တခြား output အပိုများ ထည့်မပေးရပါ။***

##### Sample Input & Output (1)
```
4
2 10
1001
9
8 16
76
0x3e
16 10
9a
154
10 8
99
0o143
```

**Input နဲ့ Output ကို ခွဲပြီးပြပါမယ်**

##### Sample Input
```
4
2 10
1001
8 16
76
16 10
9a
10 8
99
```

##### Sample Output
```
9
0x3e
154
0o143
```

<br>
<hr>

***အောက်ဖော်ပြပါ အချက်လက်များမပြည့်စုံပါက အမှတ်ရရှိမည်မဟုတ်ပါ***

* file name ကို ထုံးစံအတိုင်း email နဲ့ ထုတ်ပေးရပါမယ် (အောက်ဆုံးမှာ ထည့်ရမယ့် format ရှိပါတယ်)
* ပထမဆုံး တောင်းတဲ့ input အပါအဝင် loop ထဲမှာ တောင်းရမယ့် input တွေမှာပါ ဘာ output မှ မပြရပါ
* (example- ```num = int(input())```)
* Program ကို စိတ်ကြိုက် ရေးနိုင်ပါတယ်။ (output ကိုသာ ကန့်သတ်ထားတာပါ)
* infinite loop or မှားယွင်းတဲ့ loop ဖြစ်နေပါက အမှတ်လုံးဝမရပါ
* user ရဲ့ number အတိုင်း loop အတိအကျ ပတ်ရပါမယ်။
* Program နဲ့ စာစစ်တာဖြစ်တဲ့အတွက် output ကို Sample ပြထားသလိုပဲ ထုတ်ပေးပါခင်ဗျ။ Output အပိုထည့်တဲ့အခါ အမှတ်မရပဲ ဖြစ်တတ်ပါတယ်

**File ကို save တဲ့ အခါမှာ file name ကို အောက်ပါ Format အတိုင်း ပေးကြဖို့ အရေးကြီးပါတယ်။**

> ```asm9_(မိမိemailရှေ့ကနာမည်).py```

> *သင့်ရဲ့ email သည် ```mgmg123@gmail.com``` ဆိုပါစို့*

> ```asm9_mgmg123.py``` ဟု ပေးရမည်

> email မှာ ```'.'```(dot) တွေပါနေပါက ဖြုတ်ပြီးထည့်ပေးပါ

> ဥပမာ- email က ```kyaw.gyi.1500@gmail.com``` ဆိုရင်

> ```asm9_kyawgyi1500.py``` လို့ရေးရပါမယ်


* ***အထက်ပါအတိုင်း မှန်ကန်အောင်ပေးရမည်***
* **မသေချာလျှင် Page မှာလာပြီး မေးမြန်းပေးပါ**
* **email name/ file name မှားသူများသည် အမှတ် ရမည်မဟုတ်ပါ**

သေချာပြီဆိုလျှင် ဒီ link မှာ Assignment ထပ်ရပါမည်
[https://forms.gle/JDi7NE1DhGtbNUR28](https://forms.gle/JDi7NE1DhGtbNUR28)