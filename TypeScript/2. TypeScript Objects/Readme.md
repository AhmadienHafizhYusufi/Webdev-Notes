# Objects

```typescript
type UserObject = {
  name: string;
  age: number;
  favoriteColor: string;
};
```

OR

```typescript
interface UserObject {
  name: string;
  age: number;
  favoriteColor: string;
}
```

Creating an object type is straightforward. The syntax is virtually identical to
creating an object. You can then just apply this type to an object you create
and typescript will make sure all of those values inside are correctly typed:

```typescript
let myObject: UserObject = {
  name: "hello",
  age: 20,
  favoriteColor: "red",
};
```

If you were to change `age` to a string you'd get a Typescript Error. You would
also get a Typescript Error if you added any new keys to the object that weren't
defined in the type- or if you didn't include all the keys:

```typescript
let myObject: UserObject = {
  name: "hello",
  age: 20,
  favoriteColor: "red",
  id: 2, //error
};
```

// or

```typescript
let myObject: UserObject = {
  // error
  name: "hello",
  favoriteColor: "red",
};
```
