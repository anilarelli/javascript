# javascript

### Variables

```javascript
let username = "user1";
let loginAttempts = 3;

console.log(username);
console.log(loginAttempts);

```
### CONDITIONS (if / else)

```javascript
let attempts = 1;

if (attempts > 2) {
  console.log("Account locked");
} else {
  console.log("Account active");
}

```

```javascript

let attempts = 2;

if (attempts > 3) {
  console.log("Locked");
} else if (attempts === 3) {
  console.log("Warning");
} else {
  console.log("Safe");
}

``` 
### FUNCTIONS


```javascript

function checkAccount(attempts, isAdmin) {
  if (attempts >= 3 && !isAdmin) {
    console.log("Account locked");
  } else {
    console.log("Account active");
  }
}


checkAccount(3, false);
checkAccount(1, false);
checkAccount(5, true);

```

```javascript

function canLogin(attempts, isLocked) {
  if (attempts >= 3 || isLocked) {
    return false;
  }
  return true;
}

let canUserLogin = canLogin(2, false);
console.log(canUserLogin);
```


### loops

```javascript

for (start; condition; step) {
  // code that repeats
}
```

```javascript

for (let i = 0; i < 3; i++) {
  console.log(i);
}

```


```javascript

let attempts = 0;

while (attempts < 3) {
  console.log("Trying login...");
  attempts = attempts + 1;
}

```


```javascript

function simulateLogin(maxAttempts, isAdmin) {
  // Admin users are never locked
  if (isAdmin) {
    return false;
  }

  let attempts = 0;

  while (attempts < maxAttempts) {
    attempts++;
  }

  // If attempts reached the limit, account is locked
  return attempts >= maxAttempts;
}

simulateLogin(3, false); // true  → locked
simulateLogin(3, true);  // false → admin, not locked
simulateLogin(5, false); // true

```

### Array + object & property

```javascript
let users = [
  {id:1, name:"admin", role:"admin"},
    {id:2, name:"user", role:"user"},
    {id:3, name:"guest", role:"guest"}
]

function printusers(users){
  for (i=0; i < users.length; i++){
        
    console.log(users[i].id);
    console.log(users[i].name);
}
}
printusers(users);

```




### Return

```javascript

function addNumbers(a, b) {
  return a + b;
}

let result = addNumbers(2, 3);
console.log(result);

```

```javascript

function isEven(num) {
  if (num % 2 === 0) {
    return true;
  }
  return false;
}
let answer = isEven(4);
console.log(answer);
```



```javascript

function demo() {
  console.log(5);
  return 10;
}

let result = demo();
console.log(result);

```

```javascript

function getNumbers() {
  let arr = [1, 2, 3];
  return arr;
}

let nums = getNumbers();
console.log(nums);

```

```javascript

function getActiveUserNames(users) {
  let result = [];

  for (let i = 0; i < users.length; i++) {
    if (users[i].active === true) {
      result.push(users[i].name);
    }
  }

  return result;
}

let names = getActiveUserNames(users);
console.log(names);

```



#### Objects & Arrays (STRUCTURED DATA)

```javascript

let users = [
  { name: "admin", active: true },
  { name: "user1", active: false },
  { name: "user2", active: true }
]; 


function getactiveusers(users){
  let results = []
    for (i = 0; i < users.length; i++){
    if (users[i].active ===true){
    results.push(users[i]);
}
}
return results;
}


console.log(getactiveusers(users)); 

```









































