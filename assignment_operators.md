# Assignment Operators 

---

## Basic Assignment

| Operator | Description          | Example          | Same As |
|----------|--------------------|----------------|---------|
| `=`      | Assigns a value    | `let x = 10;`  | —       |

---

## Arithmetic Assignment

| Operator | Description             | Example      | Same As       |
|----------|------------------------|-------------|---------------|
| `+=`     | Adds and assigns       | `a += 3;`   | `a = a + 3`  |
| `-=`     | Subtracts and assigns  | `a -= 2;`   | `a = a - 2`  |
| `*=`     | Multiplies and assigns | `a *= 4;`   | `a = a * 4`  |
| `/=`     | Divides and assigns    | `a /= 2;`   | `a = a / 2`  |
| `%=`     | Remainder and assigns  | `a %= 3;`   | `a = a % 3`  |
| `**=`    | Exponentiation         | `a **= 3;`  | `a = a ** 3` |

---

## Bitwise Assignment

| Operator | Description             | Example      | Same As       |
|----------|------------------------|-------------|---------------|
| `&=`     | AND and assigns        | `a &= 3;`   | `a = a & 3`  |
| `|=`     | OR and assigns         | `a |= 2;`   | `a = a | 2`  |
| `^=`     | XOR and assigns        | `a ^= 5;`   | `a = a ^ 5`  |
| `<<=`    | Left shift and assigns | `a <<= 1;`  | `a = a << 1` |
| `>>=`    | Right shift and assigns| `a >>= 2;`  | `a = a >> 2` |
| `>>>=`   | Unsigned right shift   | `a >>>= 2;` | `a = a >>> 2` |

---

## Logical Assignment (ES2021+)

| Operator | Description                  | Example           | Same As                    |
|----------|-----------------------------|-----------------|----------------------------|
| `&&=`    | AND and assigns if truthy    | `a &&= 5;`      | `if(a) a = 5`              |
| `||=`    | OR and assigns if falsy      | `a ||= 10;`     | `if(!a) a = 10`            |
| `??=`    | Nullish coalescing assignment| `a ??= 20;`     | `if(a == null) a = 20`     |

---

## Example

```js
let a = 5;

// Arithmetic
a += 3;  // 8
a -= 2;  // 6
a *= 4;  // 24
a /= 6;  // 4
a %= 3;  // 1
a **= 3; // 1

// Bitwise
a &= 3;  // 1
a |= 2;  // 3
a ^= 1;  // 2
a <<= 1; // 4
a >>= 2; // 1
a >>>= 1;// 0

// Logical
let b;
b &&= 5;  // undefined (b is falsy)
b ||= 10; // 10
b ??= 20; // 10 (b not nullish)
