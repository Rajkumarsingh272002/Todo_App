////│── src/
│ ├── components/
│ │ ├── TodoForm.vue
│ │ ├── TodoList.vue
│ │ ├── TodoItem.vue
│ ├── App.vue
│ ├── main.jss
│── package.json

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
