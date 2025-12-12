`sizeof` ek **compile-time operator** hai jo kisi variable, datatype ya array ka **size (bytes me)** batata hai.

Neeche **bahut easy aur short points me** samjhaaya hai 👇

---

# ⭐ sizeof Kya Hai?

* `sizeof` C/C++ ka operator hai.
* Ye kisi bhi data type ka **memory size (bytes)** return karta hai.
* Code run hone se pehle **compile time** par size calculate hota hai.

---

# ⭐ Syntax

```c
sizeof(variable);
sizeof(datatype);
```

---

# ⭐ Common Examples

### 1️⃣ Primitive types

```c
sizeof(int);      // 4 bytes
sizeof(char);     // 1 byte
sizeof(float);    // 4 bytes
sizeof(double);   // 8 bytes
```

### 2️⃣ Variable ka size

```c
int x;
sizeof(x);       // same as sizeof(int)
```

### 3️⃣ Array ka size

```c
int arr[10];
sizeof(arr);     // 10 * 4 = 40 bytes
```

### 4️⃣ String (char array)

```c
char s[20];
sizeof(s);       // 20 bytes
```

---

# ⭐ Important Points

### ✔ 1. sizeof is NOT a function

* Ye **operator** hai, function nahi.
* Isliye `()` ka use optional hota hai:

```c
sizeof x;   // valid
sizeof(x);  // valid
```

### ✔ 2. Compile-time par kaam karta hai

* Runtime par koi extra cost nahi hoti.

### ✔ 3. Pointers kasizeof

```c
int *p;
sizeof(p);      // pointer ka size (4 or 8 bytes)
sizeof(*p);     // int ka size (4)
```

### ✔ 4. Array vs Pointer difference

```c
int arr[5];
int *p = arr;

sizeof(arr);  // 20 bytes
sizeof(p);    // pointer size (4 or 8 bytes)
```

---

# ⭐ Simple Diagram

Agar `int arr[4];`

```
[ 4 bytes ][ 4 bytes ][ 4 bytes ][ 4 bytes ]
Total = 16 bytes

sizeof(arr) = 16
```

---

Agar chaho to mai **quiz + practice questions** bhi de sakta hoon 👇
