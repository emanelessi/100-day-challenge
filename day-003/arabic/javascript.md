
### JavaScript
جافا سكريبت هي لغة برمجة عالية المستوى وتُفسَّر أثناء التشغيل، وتُستخدم على نطاق واسع في تطوير الويب لإنشاء عناصر تفاعلية على المواقع. تدعم تطوير الواجهة الأمامية (جهة العميل) وكذلك الواجهة الخلفية (جهة الخادم).

### 1. **المتغيرات (Variables):**
- تُستخدم لتخزين القيم. يمكنك استخدام `let` و `const` لتعريف المتغيرات.

   ```js
   let name = "Eman";  // يمكن تغيير القيمة
   const age = 28;     // ثابتة لا يمكن تغييرها
   ```

### 2. **أنواع البيانات (Data Types):**
- **الأساسية**: مثل النصوص (String)، الأرقام (Number)، القيم البوليانية (Boolean)، الكائنات (Object).
   ```js
   let str = "Hello";
   let num = 123;
   let bool = true;
   let obj = { key: "value" };
   ```

### 3. **الدوال (Functions):**
- الدوال تساعد في تجميع الأكواد القابلة لإعادة الاستخدام.
   ```js
   function greet(name) {
       return `Hello, ${name}`;
   }
   ```

**الدوال ذات التعبير السهمي (Arrow Functions):**
   ```js
   const greet = (name) => `Hello, ${name}`;
   ```

### 4. **نطاق المتغيرات (Scope):**
- **Block Scope**: المتغيرات المعرفة باستخدام `let` و `const` تكون محصورة ضمن الكتلة.
   ```js
   {
       let x = 10;
       const y = 20;
   }
   ```

### 5. **الكائنات (Objects):**
- يمكن استخدام الكائنات لتخزين البيانات بطرق منظمة.
   ```js
   const person = {
       firstName: "Eman",
       age: 28,
       greet() {
           console.log(`Hello, I'm ${this.firstName}`);
       }
   };
   person.greet();
   ```

### 6. **المصفوفات (Arrays):**
- تُستخدم لتخزين مجموعات من البيانات.
   ```js
   let arr = [1, 2, 3, 4];
   arr.push(5);  // إضافة عنصر جديد
   ```

### 7. **الحلقات (Loops):**
- **for loop**، **while loop**، و **forEach** للتكرار عبر المصفوفات.
   ```js
   for (let i = 0; i < arr.length; i++) {
       console.log(arr[i]);
   }
   ```

### 8. **التعامل مع الأخطاء (Error Handling):**
- استخدام `try...catch` لالتقاط الأخطاء والتعامل معها.
   ```js
   try {
       let result = riskyFunction();
   } catch (error) {
       console.log(error.message);
   }
   ```

### 9. **الكائنات الموجهة (Object-Oriented Programming - OOP):**
- الجافا سكريبت تدعم البرمجة الكائنية (OOP).
   ```js
   class Animal {
       constructor(name) {
           this.name = name;
       }
       speak() {
           console.log(`${this.name} makes a noise`);
       }
   }

   class Dog extends Animal {
       speak() {
           console.log(`${this.name} barks`);
       }
   }

   let dog = new Dog('Rex');
   dog.speak();
   ```

### 10. **الأحداث (Events):**
- تستخدم الأحداث للتفاعل مع المستخدم.
   ```js
   document.getElementById('myButton').addEventListener('click', function() {
       alert('Button clicked!');
   });
   ```

### 11. **التعامل مع DOM (Document Object Model):**
- **DOM** يسمح بالتفاعل مع الصفحة.
   ```js
   const title = document.getElementById('title');
   title.textContent = 'Hello World';
   ```

### 12. **التعامل مع AJAX و Fetch API:**
- يمكنك جلب البيانات من الخوادم باستخدام `fetch`.
   ```js
   fetch('https://api.example.com/data')
   .then(response => response.json())
   .then(data => console.log(data))
   .catch(error => console.log(error));
   ```

### 13. **المواعيد الزمنية (Timers):**
- يمكنك تنفيذ الأكواد بعد مدة زمنية باستخدام `setTimeout` أو بشكل متكرر باستخدام `setInterval`.
   ```js
   setTimeout(() => {
       console.log('Executed after 2 seconds');
   }, 2000);

   let interval = setInterval(() => {
       console.log('Repeated every second');
   }, 1000);
   ```

### 14. **الوعود (Promises):**
- الوعود تسهل التعامل مع العمليات غير المتزامنة.
   ```js
   const promise = new Promise((resolve, reject) => {
       let success = true;
       if (success) {
           resolve('Success!');
       } else {
           reject('Failure');
       }
   });

   promise.then(result => console.log(result)).catch(error => console.log(error));
   ```

### 15. **البرمجة غير المتزامنة (Async/Await):**
- تجعل الكود أكثر سهولة في القراءة مقارنة باستخدام الوعود.
   ```js
   async function fetchData() {
       try {
           let response = await fetch('https://api.example.com/data');
           let data = await response.json();
           console.log(data);
       } catch (error) {
           console.log(error);
       }
   }
   fetchData();
   ```

### 16. **الوحدات (Modules):**
- يمكن تقسيم الكود إلى وحدات باستخدام `export` و `import`.
   ```js
   // module.js
   export const myFunction = () => { console.log('Hello!'); };

   // main.js
   import { myFunction } from './module.js';
   myFunction();
   ```

### 17. **Advanced Topics (موضوعات متقدمة):**
- **Closure**: احتفاظ الدالة بالوصول إلى المتغيرات من نطاقها الخارجي حتى بعد انتهاء النطاق.
   ```js
   function outer() {
       let count = 0;
       return function() {
           count++;
           return count;
       };
   }
   const increment = outer();
   console.log(increment()); // 1
   console.log(increment()); // 2
   ```

- **Currying**: تحويل دالة تأخذ عدة معاملات إلى سلسلة من الدوال التي تأخذ كل منها معاملة واحدة.
   ```js
   const add = a => b => a + b;
   console.log(add(5)(3)); // 8
   ```

- **Memoization**: تحسين الأداء بتخزين نتائج العمليات المكلفة.
   ```js
   const memoizedAdd = () => {
       let cache = {};
       return (n) => {
           if (n in cache) {
               return cache[n];
           } else {
               let result = n + 10;
               cache[n] = result;
               return result;
           }
       };
   };
   const addTen = memoizedAdd();
   console.log(addTen(5)); // 15
   ```

### 18. **الخاتمة:**
JavaScript لغة قوية تتعامل مع البرمجة الكائنية والوظيفية وتدعم العمليات غير المتزامنة.


---

### تواصل معي

يمكنك متابعتي على وسائل التواصل الاجتماعي التالية:

- **Instagram:** [emanelessi](https://www.instagram.com/emanelessi/)
- **LinkedIn:** [emanelessi](https://www.linkedin.com/in/emanelessi/)

أنا متاح لأي استفسار أو تعاون في المشاريع المستقبلية. لا تتردد في التواصل معي!

