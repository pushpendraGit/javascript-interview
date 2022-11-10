# javascript-interview
Javascript Interview Question

## Question:1 - Can you pridict the output of below code?

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
## Answer:-

When we use 𝗢𝗯𝗷𝗲𝗰𝘁.𝗮𝘀𝘀𝗶𝗴𝗻 or a 𝘀𝗽𝗿𝗲𝗮𝗱 𝗼𝗽𝗲𝗿𝗮𝘁𝗼𝗿 to copy object properties, it's always a 𝘀𝗵𝗮𝗹𝗹𝗼𝘄 𝗰𝗼𝗽𝘆 operation rather than 𝗱𝗲𝗲𝗽 𝗰𝗼𝗽𝘆.

Take a look at the below code:

𝘤𝘰𝘯𝘴𝘵 𝘶𝘴𝘦𝘳 = {
𝘯𝘢𝘮𝘦: '𝘋𝘢𝘷𝘪𝘥',
𝘭𝘰𝘤𝘢𝘵𝘪𝘰𝘯: {
𝘤𝘪𝘵𝘺: '𝘕𝘠',
𝘴𝘵𝘢𝘵𝘦: '𝘕𝘠'
}
};

𝘤𝘰𝘯𝘴𝘵 𝘤𝘰𝘱𝘺 = 𝘖𝘣𝘫𝘦𝘤𝘵.𝘢𝘴𝘴𝘪𝘨𝘯({}, 𝘶𝘴𝘦𝘳);

// 𝘖𝘙
// 𝘤𝘰𝘯𝘴𝘵 𝘤𝘰𝘱𝘺 = { ...𝘶𝘴𝘦𝘳 };

𝘤𝘰𝘱𝘺.𝘭𝘰𝘤𝘢𝘵𝘪𝘰𝘯.𝘤𝘪𝘵𝘺 = '𝘈𝘭𝘣𝘢𝘯𝘺'; // change city of copy object

𝘤𝘰𝘯𝘴𝘰𝘭𝘦.𝘭𝘰𝘨('𝘰𝘳𝘪𝘨𝘪𝘯𝘢𝘭: ', 𝘶𝘴𝘦𝘳.𝘭𝘰𝘤𝘢𝘵𝘪𝘰𝘯);
𝘤𝘰𝘯𝘴𝘰𝘭𝘦.𝘭𝘰𝘨('𝘤𝘰𝘱𝘺:', 𝘤𝘰𝘱𝘺.𝘭𝘰𝘤𝘢𝘵𝘪𝘰𝘯);

The output of the above code is:

𝘰𝘳𝘪𝘨𝘪𝘯𝘢𝘭: {
𝘤𝘪𝘵𝘺: '𝘈𝘭𝘣𝘢𝘯𝘺',
𝘴𝘵𝘢𝘵𝘦: '𝘕𝘠'
}
𝘤𝘰𝘱𝘺: {
𝘤𝘪𝘵𝘺: '𝘈𝘭𝘣𝘢𝘯𝘺',
𝘴𝘵𝘢𝘵𝘦: '𝘕𝘠'
}

𝗔𝘀 𝘆𝗼𝘂 𝗰𝗮𝗻 𝘀𝗲𝗲, 𝗰𝗶𝘁𝘆 𝗼𝗳 𝗯𝗼𝘁𝗵 𝘁𝗵𝗲 𝘂𝘀𝗲𝗿.𝗹𝗼𝗰𝗮𝘁𝗶𝗼𝗻 𝗮𝗻𝗱 𝗰𝗼𝗽𝘆.𝗹𝗼𝗰𝗮𝘁𝗶𝗼𝗻 𝗼𝗯𝗷𝗲𝗰𝘁𝘀 𝗮𝗿𝗲 𝗰𝗵𝗮𝗻𝗴𝗲𝗱.

The reason for the changed original object is because when we use 𝗢𝗯𝗷𝗲𝗰𝘁.𝗮𝘀𝘀𝗶𝗴𝗻 or 𝘀𝗽𝗿𝗲𝗮𝗱 𝗼𝗽𝗲𝗿𝗮𝘁𝗼𝗿, it only does 𝘀𝗵𝗮𝗹𝗹𝗼𝘄 𝗰𝗼𝗽𝘆, which means while creating a copy of the object, properties of only the first level are copied

And if there are nested properties like city or state in the above case, then only their reference is copied which means the copied reference still refers to the original place where the object is stored.

So in our case, the location property will still refer to the original object which is a user object in our case.

# This is also one of the popularly asked question in the JavaScript interview.
