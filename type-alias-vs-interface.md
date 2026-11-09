# Type Alias এবং Interface-এর মধ্যে পার্থক্য:

# 1. Introduction

TypeScript-এ Type Alias এবং Interface দুটোই ব্যবহার করা হয় Type define করার জন্য। প্রথমে দুটিকে প্রায় একই মনে হলেও এদের মধ্যে কিছু পার্থক্য রয়েছে।

# 2. Detailed Body

*Type Alias:*

Type Alias ব্যবহার করে আমরা Object, Union, Primitive, Array, Tuple ইত্যাদির Type define করতে পারি।

```ts
type User = {
  name: string;
  age: number;
};

type Status = "success" | "error";
```

এখানে `User` দিয়ে Object-এর structure এবং `Status` দিয়ে Union Type তৈরি করেছি।

একই নামে একাধিক Type Alias declare করা যায় না। Declaration Merging-ও হয় না।

*Interface:*

Interface মূলত Object-এর structure define করার জন্য ব্যবহার করা হয়।

```ts
interface User {
  name: string;
  age: number;
}
```

Interface-এর ক্ষেত্রে একই নামে একাধিকবার declare করা যায়। তখন সেগুলো Merge হয়ে যায়। একে Declaration Merging বলে।

```ts
interface User {
  name: string;
}

interface User {
  age: number;
}
```

এখানে দুটি Interface Merge হয়ে একটি User-এর structure তৈরি করবে।

# 3. Conclusion

Type Alias এবং Interface দুটোই Object-এর structure define করতে পারে। তবে Type Alias দিয়ে Union ও Primitive-এর মতো বিভিন্ন Type তৈরি করা যায়, অন্যদিকে Interface মূলত Object-এর structure define করতে ব্যবহৃত হয়।