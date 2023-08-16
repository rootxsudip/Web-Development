# Callback que

```jsx
setTimeout(function cb() {
console.log("Hello");
},3000)
```

The above code doesn’t loaded in callstack in the first step →  setTimeout goes to web api → then goes to callback que after that it listed in the callstack list

![Screenshot_2022-01-09_11_52_44.png](Callback%20que%204ed37c489f0f4330be0865bacef6bdc0/Screenshot_2022-01-09_11_52_44.png)

![Screenshot_2022-01-09_11_54_26.png](Callback%20que%204ed37c489f0f4330be0865bacef6bdc0/Screenshot_2022-01-09_11_54_26.png)

![Screenshot_2022-01-09_11_55_38.png](Callback%20que%204ed37c489f0f4330be0865bacef6bdc0/Screenshot_2022-01-09_11_55_38.png)

![Screenshot_2022-01-09_11_57_34.png](Callback%20que%204ed37c489f0f4330be0865bacef6bdc0/Screenshot_2022-01-09_11_57_34.png)