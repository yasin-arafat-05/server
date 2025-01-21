
<br>

---

<br>

# `# Ubuntu Server Installation In Library Computer:`

<br>

---

<br>


**1.** *(select) Try or install ubuntu server.

**2.** Network Configuration: 

- **Use IPv4 Method [Automatic (DHCP)]:**
DHCP (Dynamic Host Configuration Protocol) একটি নেটওয়ার্ক প্রোটোকল যা একটি নেটওয়ার্কে যুক্ত হওয়া ডিভাইসগুলিকে 
(যেমন কম্পিউটার, স্মার্টফোন ইত্যাদি) স্বয়ংক্রিয়ভাবে আইপি ঠিকানা, সাবনেট মাস্ক, ডিফল্ট গেটওয়ে, এবং DNS সার্ভারের ঠিকানা প্রদান 
করে। এটি মূলত একটি ক্লায়েন্ট-সার্ভার মডেলে কাজ করে, যেখানে DHCP সার্ভার আইপি কনফিগারেশন প্রদান করে এবং 
ক্লায়েন্ট (যেমন আপনার কম্পিউটার) সেই কনফিগারেশন গ্রহণ করে।

- **Find Default Gateway:**
For arch linux,
```bash 
ip route
```

- **Find subnet mask and ip:**
For arch linux,
```bash
ifconfig
```

- **`Subnet Mask`  with `CIDR` Calculator in arch linux :**

First install this,
```bash 
 sudo pacman -S ipcalc
```
command format: `ipcalc <default get way> <sub net mask>`

command output:

![image](/img/img01.png)

