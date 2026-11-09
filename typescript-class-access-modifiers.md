# TypeScript Class-এর ৪টি গুরুত্বপূর্ণ Modifier:

# 1. Introduction

TypeScript-এ Class ব্যবহার করে Object তৈরি করা হয়। Class-এর Property এবং Method কোথা থেকে Access করা যাবে, তা নিয়ন্ত্রণ করার জন্য `public`, `private`, `protected` এবং `readonly` ব্যবহার করা হয়।

# 2. Detailed Body

*1. Public:*

`public` হলে Class-এর ভিতর থেকে, বাইরে থেকে এবং Subclass থেকে Access করা যায়।

```ts
class User {
  public name = "Arman";
}

const user = new User();
console.log(user.name);
```

*2. Private:*

`private` হলে শুধু নিজের Class-এর ভিতর থেকে Access করা যায়। বাইরে থেকে বা Subclass থেকে Access করা যায় না।

```ts
class User {
  private age = 23;
}
```

**3. Protected:**

`protected` হলে নিজের Class এবং Subclass থেকে Access করা যায়। বাইরে থেকে Access করা যায় না।

```ts
class User {
  protected name = "Arman";
}

class Student extends User {
  showName() {
    console.log(this.name);
  }
}
```

*4. Readonly:*

`readonly` Property-এর Value একবার Set করার পর পুনরায় পরিবর্তন করা যায় না। তবে Declaration-এর সময় অথবা Constructor-এর মাধ্যমে Value দেওয়া যায়।

```ts
class User {
  readonly name = "Arman";
}

const user = new User();
console.log(user.name);

// user.name = "Sabbir"; // Error
```

# 3. Conclusion

TypeScript Class-এ `public`, `private` এবং `protected` ব্যবহার করে Property ও Method-এর Access নিয়ন্ত্রণ করা যায়। অন্যদিকে `readonly` ব্যবহার করে কোনো Property-এর Value পরিবর্তন হওয়া থেকে রক্ষা করা যায়।

মনে রাখতে হবে, `readonly` একটি Property Modifier, Access Modifier নয়।