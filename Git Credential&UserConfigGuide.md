
# Git Credential & User Config Guide

এই ডকুমেন্টে Git-এর কিছু গুরুত্বপূর্ণ কমান্ডের কাজ ব্যাখ্যা করা হলো।  
এগুলো ব্যবহার করে আপনি আপনার GitHub credential এবং user identity ম্যানেজ করতে পারবেন।

---

## 1. পুরনো ইউজারনেম/ইমেইল আনসেট করা

### কমান্ড
```bash
git config --global --unset user.name
git config --global --unset user.email
```

### কাজ
- **user.name আনসেট:** global Git configuration থেকে `user.name` মুছে দেয়।
- **user.email আনসেট:** global Git configuration থেকে `user.email` মুছে দেয়।

### কখন ব্যবহার করবেন
- পুরনো বা ভুলভাবে সেট করা নাম/ইমেইল রিসেট করতে হলে।

---

## 2. Windows Credential Manager থেকে GitHub credential মুছে ফেলা

### কমান্ড
```bash
git credential-manager erase
```

এরপর নিচের ইনপুট দিন:
```text
protocol=https
host=github.com
username=your-username
```

### কাজ
- নির্দিষ্ট host (`github.com`) এবং আপনার username অনুযায়ী সংরক্ষিত credential মুছে দেয়।

### নোট
- `your-username` এর জায়গায় আপনার আসল GitHub username দিন (উদাহরণ: `m-anwarulkarim`)।
- মুছে ফেলার পর পরবর্তী `git push/pull` এ নতুন credential চাইবে (PAT ব্যবহার করা উত্তম)।

---

## 3. নতুন ইউজারনেম/ইমেইল সেট করা

### কমান্ড
```bash
git config --global user.name "anwarul karim"
git config --global user.email "dev.anwarul@gmail.com"
```

### কাজ
- **user.name সেট:** আপনার কমিটগুলোতে প্রদর্শিত নাম নির্ধারণ করে।
- **user.email সেট:** আপনার কমিটগুলো GitHub প্রোফাইলের সাথে সঠিকভাবে লিঙ্ক হতে সাহায্য করে।

### টিপস
- ইমেইলটি আপনার GitHub অ্যাকাউন্টে ব্যবহৃত/ভেরিফাইড ইমেইল হওয়া উচিত।
- প্রয়োজন হলে চেক করুন:
  ```bash
  git config --get user.name
  git config --get user.email
  ```

---

## ✅ সারসংক্ষেপ (ধাপে ধাপে)

1. **পুরনো কনফিগ আনসেট করুন:**  
   ```bash
   git config --global --unset user.name
   git config --global --unset user.email
   ```

2. **পুরনো credential মুছে ফেলুন:**  
   ```bash
   git credential-manager erase
   ```
   তারপর ইনপুট দিন:
   ```text
   protocol=https
   host=github.com
   username=your-username
   ```

3. **নতুন কনফিগ সেট করুন:**  
   ```bash
   git config --global user.name "anwarul karim"
   git config --global user.email "dev.anwarul@gmail.com"
   ```

4. **যাচাই করুন:**  
   ```bash
   git config --list
   ```

---

## ℹ️ অতিরিক্ত তথ্য

 Windows Credential Manager থেকে GitHub Credential মুছে ফেলার ধাপ

1. **Start Menu** খুলুন  
2. **Control Panel** এ যান  
3. **Credential Manager** ওপেন করুন  
4. **Windows Credentials** সেকশনে যান  
5. সেখানে **GitHub এন্ট্রি** খুঁজে বের করুন  
6. সেটি সিলেক্ট করে **Remove** করুন
 
- **Error এলে:**  
  - `git push` এর সময় credential চাইলে PAT ব্যবহার করুন।  
  - প্রয়োজন হলে remote চেক করুন:
    ```bash
    git remote -v
    ```

---

**Author:** *ANWARUL KARIM*  
**Updated:** 2025
