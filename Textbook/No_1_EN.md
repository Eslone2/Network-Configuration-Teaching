**Please note:** There may be mistranslations in the English version. We ask for your understanding.

## 💻 Network Installation/Building Workshop (1st Session)



### 🎯 The Main Topics for This Time

* **Understanding the mechanism of IP addresses, subnet masks, and network addresses.**
* What roles do routers and L2 switches play within a network system? (This may be covered in a future session.)

---

### 📥 Before Diving Into the Main Topic...

We need to check if you have **"TeraTerm"** installed on your PC (especially Windows).

If you haven't installed it, please click [**here**](https://github.com/TeraTermProject/teraterm/releases) to download and install!

> **Note:** This tool is planned to be used from the second session onwards. Please **do not** uninstall it!

---

### 🌐 How IP Addresses, Subnet Masks, and Network Addresses Work

#### **What is an IP Address?**

An IP address is (in simple terms) like an **"address on the internet"**!

Also, **IP addresses must absolutely not be duplicated** as this will prevent communication.

For example, consider sending a letter:
* **Sender's address:** Aomori City, Aomori Prefecture, XX-cho, x-chome, x-x
* **Recipient's address:** Hachinohe City, Aomori Prefecture, xx-cho, x-chome, x-x

If we replace these addresses with IP addresses:
* **Sending Device:** `172.155.10.1`
* **Receiving Device:** `153.128.11.1`

This is the basic idea (though there are subtle differences).

> **Note:** The explanation here will primarily use **IPv4**. We will cover **IPv6** later! (**IPv4** operates on 32 bits.)

* The abbreviation **"IP Address"** stands for **Internet Protocol Address**. (We will explain Protocol later!)
* Simply put, it's a **method of writing an address that adheres to the rules (Protocol) of the internet.** We will explain later where IP addresses are utilized.

#### **Network Part and Host Part**

* The **Network Part** is the number that indicates **which network a device belongs to**! Think of it like the apartment building name (e.g., **172.155.10**.1).
* The **Host Part** is the number that indicates **which specific device** within the above network! Think of it like the "room number" (e.g., 172.155.10.**1**).

> **Example:** In the example `172.155.10.1`, the **bold** part is the Network Part, and the part in regular font is the Host Part.

> **FYI:** IP addresses are determined by country and region.
> *Reference: [IP Address - The IT Terminology Dictionary](https://wa3.i-3-i.info/word172.html)*

#### **What is a Subnet Mask?**

A Subnet Mask is an **instruction manual on how to distinguish between the Network Part and the Host Part**.

> *Reference: [Subnet Mask - The IT Terminology Dictionary](https://wa3.i-3-i.info/word11975.html)*

A Subnet Mask can be determined through calculation.

For example, if the subnet mask is `255.255.255.0`.
Converting this to **binary** (only 0s and 1s) results in: `11111111.11111111.11111111.00000000`.

* The part marked in **bold** (`11111111.11111111.11111111`.00000000) is the **Network Part**.
* The part marked in **bold** (11111111.11111111.11111111.**00000000**) is the **Host Part**.

---

### 📝 Exercise: Separating Network and Host Parts

Now, let's practice separating the Network Part and the Host Part.

1. For the IP address **`192.168.0.2`** with a subnet mask of **`255.255.0.0`**.
2. For the IP address **`192.168.163.1`** with a subnet mask of **`11111111.00000000.00000000.00000000`** (binary).

---

### ✅ Answers

1. **IP Address:** `192.168.0.2`
   **Subnet Mask:** `255.255.0.0`
   * **Network Part:** `192.168`
   * **Host Part:** `0.2`

2. **IP Address:** `192.168.163.1`
   **Subnet Mask (Decimal):** `255.0.0.0`
   * **Network Part:** `192`
   * **Host Part:** `168.163.1`
