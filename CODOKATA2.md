## Pythonスキルをまんべんなく磨く10個のCode Kata

Pythonのスキルをまんべんなく磨くためのCode Kataを10個作成しました。詳細な回答例と最短コード例を記載します。

### 1. 文字列の反転

**問題:** 文字列を反転させる関数を作成してください。

**詳細な回答例:**

```python
def reverse_string(s):
  return s[::-1]

print(reverse_string("hello"))  # 出力: olleh
```

**最短コード例:**

```python
reverse_string = lambda s: s[::-1]

print(reverse_string("hello"))  # 出力: olleh
```

### 2. 回文判定

**問題:** 文字列が回文かどうかを判定する関数を作成してください。

**詳細な回答例:**

```python
def is_palindrome(s):
  s = s.lower().replace(" ", "")
  return s == s[::-1]

print(is_palindrome("racecar"))  # 出力: True
print(is_palindrome("A man, a plan, a canal: Panama"))  # 出力: True
```

**最短コード例:**

```python
is_palindrome = lambda s: (s := s.lower().replace(" ", "")) == s[::-1]

print(is_palindrome("racecar"))  # 出力: True
print(is_palindrome("A man, a plan, a canal: Panama"))  # 出力: True
```

### 3. フィボナッチ数列

**問題:** n番目のフィボナッチ数を返す関数を作成してください。

**詳細な回答例:**

```python
def fibonacci(n):
  if n <= 0:
    return 0
  elif n == 1:
    return 1
  else:
    a, b = 0, 1
    for _ in range(n - 1):
      a, b = b, a + b
    return a

print(fibonacci(10))  # 出力: 34
```

**最短コード例:**

```python
fibonacci = lambda n: n if n <= 1 else fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(10))  # 出力: 55 (再帰呼び出しのため効率は悪い)
```

### 4. 素数判定

**問題:** nが素数かどうかを判定する関数を作成してください。

**詳細な回答例:**

```python
def is_prime(n):
  if n <= 1:
    return False
  for i in range(2, int(n**0.5) + 1):
    if n % i == 0:
      return False
  return True

print(is_prime(17))  # 出力: True
print(is_prime(12))  # 出力: False
```

**最短コード例:**

```python
is_prime = lambda n: n > 1 and all(n % i for i in range(2, int(n**0.5) + 1))

print(is_prime(17))  # 出力: True
print(is_prime(12))  # 出力: False
```

### 5. リストの重複削除

**問題:** リストから重複要素を削除する関数を作成してください。

**詳細な回答例:**

```python
def remove_duplicates(lst):
  return list(set(lst))

print(remove_duplicates([1, 2, 2, 3, 4, 4, 5]))  # 出力: [1, 2, 3, 4, 5]
```

**最短コード例:**

```python
remove_duplicates = lambda lst: list(set(lst))

print(remove_duplicates([1, 2, 2, 3, 4, 4, 5]))  # 出力: [1, 2, 3, 4, 5]
```

### 6. 文字列の単語数カウント

**問題:** 文字列中の単語数をカウントする関数を作成してください。

**詳細な回答例:**

```python
def count_words(s):
  return len(s.split())

print(count_words("This is a test string."))  # 出力: 5
```

**最短コード例:**

```python
count_words = lambda s: len(s.split())

print(count_words("This is a test string."))  # 出力: 5
```

### 7. 最大公約数 (GCD)

**問題:** 2つの整数の最大公約数を求める関数を作成してください。

**詳細な回答例:**

```python
def gcd(a, b):
  while b:
    a, b = b, a % b
  return a

print(gcd(48, 18))  # 出力: 6
```

**最短コード例:**

```python
gcd = lambda a, b: gcd(b, a % b) if b else a

print(gcd(48, 18))  # 出力: 6
```

### 8. 最小公倍数 (LCM)

**問題:** 2つの整数の最小公倍数を求める関数を作成してください。

**詳細な回答例:**

```python
def lcm(a, b):
  return (a * b) // gcd(a, b)

print(lcm(12, 18))  # 出力: 36
```

**最短コード例:**

```python
lcm = lambda a, b: (a * b) // gcd(a, b)

print(lcm(12, 18))  # 出力: 36
```

### 9. 階乗

**問題:** nの階乗を求める関数を作成してください。

**詳細な回答例:**

```python
def factorial(n):
  if n == 0:
    return 1
  else:
    return n * factorial(n-1)

print(factorial(5))  # 出力: 120
```

**最短コード例:**

```python
factorial = lambda n: 1 if n == 0 else n * factorial(n-1)

print(factorial(5))  # 出力: 120
```

### 10. リストのflatten

**問題:** ネストされたリストをフラットにする関数を作成してください。

**詳細な回答例:**

```python
def flatten(lst):
  result = []
  for item in lst:
    if isinstance(item, list):
      result.extend(flatten(item))
    else:
      result.append(item)
  return result

print(flatten([1, [2, 3], [4, [5, 6]]]))  # 出力: [1, 2, 3, 4, 5, 6]
```

**最短コード例:**

```python
flatten = lambda lst: sum([flatten(x) if isinstance(x, list) else [x] for x in lst], [])

print(flatten([1, [2, 3], [4, [5, 6]]]))  # 出力: [1, 2, 3, 4, 5, 6]
```

これらのCode Kataは、Pythonの基本的なスキルを網羅しており、繰り返し練習することで、より実践的なスキルを身につけることができます。
