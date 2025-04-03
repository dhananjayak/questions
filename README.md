
---

### **Question Set 1: React & TypeScript**  

#### **1. What is the correct TypeScript type for a React component's props that expects a `title` (string) and `onClick` (function)?**  
A) `type Props = { title: any, onClick: any }`  
B) `interface Props { title: string; onClick: () => void }`  
C) `type Props = { title: string, onClick: function }`  
D) `interface Props { title: string; onClick: () => any }`  

#### **2. (Coding) Fix this React hook to fetch data:**  
```tsx
const [data, setData] = useState(null);
useEffect(async () => {
  const res = await fetch('https://api.example.com/data');
  setData(res.json()); 
}, []);
```  
**Options for correction:**  
A) Remove `async` from `useEffect` and use `.then()`  
B) Add `res.json()` inside a `try-catch`  
C) Move `async` inside the effect and await `res.json()`  
D) Both A and C  

#### **3. (Coding) Write a TypeScript function to filter even numbers from an array:**  
```ts
function filterEvens(arr: number[]): number[] {
  // Your code here
}
```  

#### **4. (Coding) How would you type a React event handler for an input change?**  
A) `(e: Event) => void`  
B) `(e: React.SyntheticEvent) => void`  
C) `(e: React.ChangeEvent<HTMLInputElement>) => void`  
D) `(e: any) => void`  

#### **5. (Coding) Fix this TypeScript interface for a `User` with optional `age`:**  
```ts
interface User {
  name: string;
  // Your fix here
}
```  

---

### **Question Set 2: Node.js & Databases**  

#### **6. Which SQL query finds all users with more than 10 orders?**  
A) `SELECT * FROM users WHERE orders > 10`  
B) `SELECT * FROM users JOIN orders ON users.id = orders.user_id HAVING COUNT(orders.id) > 10`  
C) `SELECT * FROM users WHERE (SELECT COUNT(*) FROM orders WHERE user_id = users.id) > 10`  
D) Both B and C  

#### **7. (Coding) Write an Express route to handle a POST request to `/api/login`:**  
```js
app.post('/api/login', (req, res) => {
  // Your code here
});
```  

#### **8. (Coding) Fix this SQL injection-prone query:**  
```js
// Vulnerable:
db.query(`SELECT * FROM users WHERE email = '${email}'`);
// Corrected:
// Your fix here
```  

#### **9. (Coding) Write a middleware to log request methods in Express:**  
```js
app.use((req, res, next) => {
  // Your code here
});
```  

#### **10. (Coding) Which JOIN type returns all rows from the left table, even if no matches exist?**  
A) `INNER JOIN`  
B) `LEFT JOIN`  
C) `RIGHT JOIN`  
D) `FULL OUTER JOIN`  

---

### **Question Set 3: Data Structures**  

#### **11. What is the time complexity of inserting at the end of a dynamic array?**  
A) O(1) (amortized)  
B) O(n)  
C) O(log n)  
D) O(n²)  

#### **12. (Coding) Implement a stack using an array:**  
```js
class Stack {
  constructor() {
    // Your code here
  }
  push(item) {
    // Your code here
  }
  pop() {
    // Your code here
  }
  peek() {
    // Your code here
  }
}
```  

#### **13. (Coding) Write a function to reverse a linked list:**  
```js
function reverseList(head) {
  // Your code here
}
```  

#### **14. (Coding) Fix this binary search function:**  
```js
function binarySearch(arr, target) {
  let left = 0, right = arr.length - 1;
  while (left <= right) {
    const mid = Math.floor((left + right) / 2);
    if (arr[mid] === target) return mid;
    if (arr[mid] < target) left = mid + 1;
    else right = mid - 1;
  }
  return -1;
}
```  

#### **15. (Coding) What is the output of this closure code?**  
```js
function createCounter() {
  let count = 0;
  return () => ++count;
}
const counter = createCounter();
console.log(counter(), counter()); // Output: ?
```  

---

### **Answer Key**  

#### **Question Set 1 Answers**  
1. **B** – `interface Props { title: string; onClick: () => void }`  
2. **D** – Both A and C (use `.then()` or `try-catch`)  
3. **Solution:**  
   ```ts
   return arr.filter(num => num % 2 === 0);
   ```  
4. **C** – `(e: React.ChangeEvent<HTMLInputElement>) => void`  
5. **Solution:**  
   ```ts
   age?: number;
   ```  

#### **Question Set 2 Answers**  
6. **D** – Both B and C  
7. **Solution:**  
   ```js
   const { email, password } = req.body;
   res.status(200).json({ success: true });
   ```  
8. **Solution:**  
   ```js
   db.query('SELECT * FROM users WHERE email = ?', [email]);
   ```  
9. **Solution:**  
   ```js
   console.log(`${req.method} ${req.url}`);
   next();
   ```  
10. **B** – `LEFT JOIN`  

#### **Question Set 3 Answers**  
11. **A** – O(1) (amortized)  
12. **Solution:**  
    ```js
    this.items = [];
    this.items.push(item);
    return this.items.pop();
    return this.items[this.items.length - 1];
    ```  
13. **Solution:**  
    ```js
    let prev = null;
    while (head) {
      const next = head.next;
      head.next = prev;
      prev = head;
      head = next;
    }
    return prev;
    ```  
14. **Solution:** Already correct.  
15. **Output:** `1, 2`  

---

### **Formatting Notes for Word**  
1. **Headings**: Use **Heading 1** for "Question Set X" and **Heading 2** for questions.  
2. **Code Blocks**: Use a monospace font (e.g., Consolas) and gray background.  
3. **Lists**: Use bullet points for options (A, B, C, D).  
4. **Answer Key**: Use a table for clarity.  

Let me know if you'd like further adjustments!# questions
