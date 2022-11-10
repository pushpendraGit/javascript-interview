# javascript-interview
Javascript Interview Question

## Can you pridict the output of below code?

```

const user = {
    name: 'Pushpendra',
    location: {
        city: 'NY',
        state: 'NY'
    }
}

const copy = {...user}

copy.loaction.city = 'Albany'

console.log(user);
console.log(copy)

```
