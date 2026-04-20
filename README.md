# 🔗 HashSet Custom Implementation (C#)

A custom implementation of a **generic HashSet** built from scratch using **C#**.

This project was developed as part of my studies in **Data Structures**, focusing on understanding how hashing, collision handling, and performance optimization work internally.

---

## 🚀 Features

* Generic implementation (`HashSetCustom<T>`)
* Constant time complexity for most operations (**O(1)** average)
* Collision handling using **chaining (Linked List)**
* Custom equality support via `IEqualityComparer<T>`
* Core operations:

  * `Add`
  * `Remove`
  * `Contains`
  * `Clear`
* Fully covered with unit tests (NUnit)

---

## 🧠 How It Works

This HashSet uses:

* **Hashing** (`GetHashCode`) to map values to indices
* **Buckets (array)** to store elements
* **Chaining (Linked Lists)** to handle collisions

### Example:

```
Index → Bucket
0 → [10 → 20]
1 → [5]
2 → []
```

---

## ⚙️ Core Implementation

### Index Calculation

```csharp
private int GetIndex(T value)
{
    int hash = _compare.GetHashCode(value);
    return (hash & 0x7FFFFFFF) % _buckets.Length;
}
```

* Ensures positive hash values
* Distributes elements across buckets

---

## 📊 Time Complexity

| Operation | Complexity   |
| --------- | ------------ |
| Add       | O(1) average |
| Remove    | O(1) average |
| Contains  | O(1) average |

> Worst case: O(n) (when many collisions occur)

---

## 🧪 Unit Tests

This project includes a comprehensive test suite using **NUnit**, covering:

* Element insertion
* Duplicate handling
* Removal behavior
* Collision scenarios
* Clear operation
* Generic type support
* State consistency after multiple operations

---

## 🛠️ Technologies

* C#
* .NET
* NUnit

---

## 🎯 Purpose

This project was built to:

* Deeply understand how **HashSet** works internally
* Practice **data structures implementation**
* Improve knowledge of **generics and hashing**
* Strengthen problem-solving and algorithmic thinking

---

## 📌 Future Improvements

* Dynamic resizing (rehashing)
* Performance optimizations
* IEnumerable support
* Custom load factor control

---

## 👨‍💻 Author

Thiago Santiago Rodrigues

---

## ⭐ Final Thoughts

This implementation demonstrates how a HashSet can be built from scratch, including handling collisions and ensuring efficient operations.

> Understanding the internal mechanics of data structures is essential for writing efficient and scalable code.

