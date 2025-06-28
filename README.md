Project का Name और Aim => This is simple "todo" app for beginner learning purpose. main ojective is that you insert any text related to simple work such that anyone name you write or any message you write or pets names you write .this type of work you can do.
..............................................................................

ScreenShot=>
![Image](https://github.com/user-attachments/assets/52188601-2e7d-40e2-8e58-c63e0ee33a42)
![Image](https://github.com/user-attachments/assets/f3c723b5-c37d-4d0d-8c18-85392eb5df01)
![Image](https://github.com/user-attachments/assets/003e2c5a-6e89-4404-8a9b-223b2ee16ffe)



..............................................................................................

Project Structure=>
│──src/
│ ├── components/
│ │ ├── TodoForm.vue
│ │ ├── TodoList.vue
│ │ ├── TodoItem.vue
│ ├── App.vue
│ ├── main.jss
│── package.json

..................................................................................................

Features=>
1-TodoForm.vue → नया टास्क जोड़न क लए
2 TodoItem.vue → एक-एक टास्क को दखान और actions (complete/delete) करन क लए
3 TodoList.vue → सार टास्क को लस्ट क रूप म दखान क लए
4-App.vue → Parent component जो इन सबको मनज करगा

1->TodoForm.vue → नया टास्क जोड़न क लए
�इसका काम क्या ह?
✅
newTodo → यह input field को track करता ह।
✅
जब "Enter" दबाया जाता ह या "
➕
जोड़" बटन िक्लक होता ह, तो event emit करता ह।
✅
Parent (App.vue) इस event को सनकर todos list म नया टास्क जोड़ दगा।

2->TodoItem.vue → एक-एक टास्क को दखान और actions (complete/delete) करन क लए
�इसका काम क्या ह?
✅
यह todo को display करता ह।
✅
Complete/Incomplete toggle करन क लए toggleComplete event emit करता ह।
✅
Delete करन क लए deleteTodo event emit करता ह।

3->TodoList.vue → सार टास्क को लस्ट क रूप म दखान क लए
�इसका काम क्या ह?
✅
यह todos1 array को loop करक Todo म भजता ह।
✅
अगर कोई event emit होता ह (toggle-complete2 या delete-todo2), तो यह उस Parent (App.vue)
को forward करता ह।

4->App.vue (Main Component - लास्ट म दखगा!)
�इसका काम क्या ह?
✅
todos list को track करता ह।
✅
TodoForm स event आन पर नया टास्क जोड़ता ह।
newTodo data goto app.vue(todos.value.push({ text: todoText.trim(), completed: false });) by app.vue(<TodoForm @add-todo="addTodo"/>)
✅
TodoList स event आन पर toggle या delete करता ह।
✅

..............................................................................................................................

कैसे चलाएं (install/run

0-  make folder (todoApp) on desktop and select path of (todoApp) folder such that like this (\Users\Rajkumar\Desktop\todoApp).

1-opend cmd-command and type (cd ..) then enter like this you continue (cd ..) when till you will not  found c:\ and in last you cmd-command look c:/

2-you cmd-command look like this:
  c:/
  and paste this path(\Users\Rajkumar\Desktop\todoApp) then you see of cmd look like this:
  c:\Users\Rajkumar\Desktop\todoApp   
  
3- Create Project using vue.js 
    you type(npm create vue@latest) into cmd like this:
  C:\Users\Rajkumar\Desktop\todoApp>npm create vue@latest
  
  (npm create vue@latest क्या करता है ये command?
  यह command Vue.js का latest starter setup बनाता है, यानी:
  Vite के साथ Vue project
  Project name, TypeScript, Router, Pinia आदि setup options)

4-फिर यह पूछेगा:

✔ Project name: … todo
✔ Add TypeScript? … No
✔ Add Vue Router for Single Page Application development? … Yes
✔ Add Pinia for state management? … Yes
✔ Add Vitest for Unit Testing? … No
✔ Add Cypress for Testing? … No
✔ Add ESLint for code quality? … Yes


5-इसके बाद ये command चलाएं:
  -> cd todo
  -> npm install
  -> npm run dev

6-open browser and type (http://localhost:5173/) into browser address bar
.............................................................................................................................

Tech Stack=> (HTML, css3, bootstrap5, vue.js3 composition-api)
