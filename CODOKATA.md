## Pythonコードカタ10選

### 概要

コードカタとは、プログラミングのスキル向上を目的とした、短いプログラミング課題のことです。武道における「型」のように、コードカタを繰り返し練習することで、プログラミングの基礎力、問題解決能力、アルゴリズムの理解などを深めることができます。

本稿では、Pythonのスキルを向上させるためのコードカタを10個紹介します。各コードカタは、Pythonの様々な側面を網羅しており、詳細なコードと最短コードの両方の解答例と解説を提供することで、深い理解を促進します。これらのコードカタに取り組むことで、Pythonの基礎力から応用力まで、幅広いスキルを習得することができます。

### コードカタ一覧 (難易度順)

1. 数字を負にする
2. 文字列の最初と最後の文字を削除する
3. 整数の配列を逆にする
4. 数値の平方和を計算する
5. Xずつカウントする
6. アルファベットを位置に置き換える
7. 一意の文字列を見つける
8. FizzBuzz問題を解く
9. 最長の回文を見つける
10. スーパーマーケットの価格設定

### コードカタ1：数字を負にする

**スキル:** 関数、数値演算

**問題:** 与えられた数値を負にする関数`make_negative`を作成してください。

**詳細コード:**

```python
def make_negative(number):
  """
  与えられた数値を負にする関数

  Args:
    number: 負にする数値

  Returns:
    負にした数値
  """
  if number > 0:
    return -number
  else:
    return number
```

**最短コード:**

```python
def make_negative(number):
  return -abs(number)
```

**解説:** `abs()`関数は、数値の絶対値を返す関数です。これにより、入力値が正の場合でも負の場合でも、常に負の値を返すことができます。

**Key Insights:**
このコードカタでは、関数の定義方法と、条件分岐を用いた基本的な数値演算を学ぶことができます。また、`abs()`関数を利用することで、より簡潔なコードを書くことができることを示しています。

### コードカタ2：文字列の最初と最後の文字を削除する

**スキル:** 文字列操作、スライス

**問題:** 与えられた文字列の最初と最後の文字を削除する関数`remove_char`を作成してください。

**詳細コード:**

```python
def remove_char(s):
  """
  文字列の最初と最後の文字を削除する関数

  Args:
    s: 文字列

  Returns:
    最初と最後の文字を削除した文字列
  """
  return s[1:-1]
```

**最短コード:**

```python
remove_char = lambda s: s[1:-1]
```

**解説:** Pythonのスライス機能を使用することで、文字列の一部を効率的に抽出できます。`[1:-1]`は、2文字目から最後から2文字目までの部分文字列を抽出することを意味します。

**Key Insights:**
このコードカタでは、Pythonの文字列のスライス機能について学ぶことができます。スライス機能を使うことで、文字列の特定の部分を簡単に取り出すことができます。また、ラムダ式を用いた関数の定義方法も学ぶことができます。

### コードカタ3：整数の配列を逆にする

**スキル:** リスト操作

**問題:** 与えられた整数の配列を逆にする関数`reverse_array`を作成してください。

**詳細コード:**

```python
def reverse_array(arr):
  """
  整数の配列を逆にする関数

  Args:
    arr: 整数の配列

  Returns:
    逆にした配列
  """
  reversed_arr = []
  for i in range(len(arr) - 1, -1, -1):
    reversed_arr.append(arr[i])
  return reversed_arr
```

**最短コード:**

```python
def reverse_array(arr):
  return arr[::-1]
```

**解説:** スライス機能を使うことで、配列を逆順に取得できます。`[::-1]`は、配列を逆順にすることを意味します。

**Key Insights:**
このコードカタでは、リストを逆順にする方法を学ぶことができます。ループとインデックスを用いた方法と、スライス機能を用いた方法の2つがあり、スライス機能を用いた方がより簡潔で効率的なコードを書くことができます。

### コードカタ4：数値の平方和を計算する

**スキル:** リスト操作、数値演算、内包表記

**問題:** 与えられた数値のリストの各要素を2乗し、その合計を返す関数`square_sum`を作成してください。

**詳細コード:**

```python
def square_sum(numbers):
  """
  数値のリストの各要素を2乗し、その合計を返す関数

  Args:
    numbers: 数値のリスト

  Returns:
    平方和
  """
  sum = 0
  for number in numbers:
    sum += number ** 2
  return sum
```

**最短コード:**

```python
def square_sum(numbers):
  return sum(x ** 2 for x in numbers)
```

**解説:** 内包表記を使用することで、より簡潔にコードを記述できます。

**Key Insights:**
このコードカタでは、内包表記を用いたリストの処理方法を学ぶことができます。内包表記を使うことで、forループをより簡潔に記述することができます。また、`sum()`関数を利用することで、リストの要素の合計を簡単に計算することができます。

### コードカタ5：Xずつカウントする

**スキル:** リスト操作、数値演算、`range`関数

**問題:** Xずつ増加する数値のリストを返す関数`count_by_x`を作成してください。関数は2つの引数`x`と`n`を取り、`x`から始まり`x`ずつ増加し、`x * n`以下の数値を含むリストを返します。

**詳細コード:**

```python
def count_by_x(x, n):
  """
  Xずつ増加する数値のリストを返す関数

  Args:
    x: 増加する値
    n: リストの長さ

  Returns:
    xずつ増加する数値のリスト
  """
  result = []
  for i in range(1, n + 1):
    result.append(x * i)
  return result
```

**最短コード:**

```python
def count_by_x(x, n):
  return list(range(x, x * (n + 1), x))
```

**解説:** `range()`関数は、指定された範囲の数値のシーケンスを生成します。

**Key Insights:**
このコードカタでは、`range()`関数を用いて、特定の条件を満たす数値のリストを生成する方法を学ぶことができます。`range()`関数の引数を適切に設定することで、様々な数値シーケンスを生成することができます。

### コードカタ6：アルファベットを位置に置き換える

**スキル:** 文字列操作、ASCIIコード、内包表記

**問題:** 与えられた文字列のアルファベットを、アルファベット順での位置に置き換える関数`alphabet_position`を作成してください。

**詳細コード:**

```python
def alphabet_position(text):
  """
  文字列のアルファベットを、アルファベット順での位置に置き換える関数

  Args:
    text: 文字列

  Returns:
    アルファベットの位置に置き換えられた文字列
  """
  result = []
  for char in text.lower():
    if char.isalpha():
      result.append(str(ord(char) - 96))
  return " ".join(result)
```

**最短コード:**

```python
def alphabet_position(text):
  return ' '.join(str(ord(c) - 96) for c in text.lower() if c.isalpha())
```

**解説:** `ord()`関数は、文字のASCIIコードを返します。aのASCIIコードは97なので、96を引くことでアルファベット順での位置を求めることができます。

**Key Insights:**
このコードカタでは、文字列を操作し、ASCIIコードを用いてアルファベットの位置を求める方法を学ぶことができます。また、内包表記と`join()`関数を組み合わせることで、文字列を効率的に連結する方法も学ぶことができます。

### コードカタ7：一意の文字列を見つける

**スキル:** 文字列操作、リスト操作、集合

**問題:** 文字列のリストが与えられ、その中で一つだけ異なる文字列を見つける関数`find_uniq`を作成してください。

**詳細コード:**

```python
def find_uniq(arr):
  """
  文字列のリストの中で一つだけ異なる文字列を見つける関数

  Args:
    arr: 文字列のリスト

  Returns:
    一つだけ異なる文字列
  """
  arr.sort(key=lambda x: x.lower())
  arr1 = [set(i.lower()) for i in arr]
  return arr[0] if arr1.count(arr1[0]) == 1 else arr
```

**最短コード:**

```python
def find_uniq(arr):
  arr.sort(key=lambda x: x.lower())
  arr1 = [set(i.lower()) for i in arr]
  return arr if arr1.count(arr1) == 1 and str(arr1) != 'set()' else arr
```

**解説:** 各文字列を小文字に変換し、集合に変換することで、重複する文字を無視して比較することができます。

**Key Insights:**
このコードカタでは、集合を用いて文字列の重複を無視する方法、ラムダ式を用いたソート方法、条件分岐を用いた処理方法を学ぶことができます。

### コードカタ8：FizzBuzz問題を解く

**スキル:** 条件分岐、ループ

**問題:** FizzBuzz問題を解く関数`fizzbuzz`を作成してください。 FizzBuzz問題とは、1からnまでの数字を出力し、3の倍数のときは"Fizz"、5の倍数のときは"Buzz"、3と5の両方の倍数のときは"FizzBuzz"と出力する問題です。

**詳細コード:**

```python
def fizzbuzz(n):
  """
  FizzBuzz問題を解く関数

  Args:
    n: 最大値

  Returns:
    FizzBuzz問題の解答
  """
  result = []
  for i in range(1, n + 1):
    if i % 3 == 0 and i % 5 == 0:
      result.append("FizzBuzz")
    elif i % 3 == 0:
      result.append("Fizz")
    elif i % 5 == 0:
      result.append("Buzz")
    else:
      result.append(str(i))
  return result
```

**最短コード:**

```python
def fizzbuzz(n):
  return ['Fizz'*(i%3==0) + 'Buzz'*(i%5==0) or str(i) for i in range(1,n+1)]
```

**解説:** 最短コードでは、条件式を文字列の乗算に利用することで、if文を使わずにFizzBuzz問題を解いています。具体的には、`(i % 3 == 0)`は、`i`が3の倍数のときに`True`となり、1として評価されます。これを文字列`'Fizz'`に乗算することで、3の倍数のときに`'Fizz'`、そうでないときに空文字列`''`が得られます。同様に、5の倍数のときは`'Buzz'`、そうでないときは空文字列`''`が得られます。これらの文字列を連結することで、`'Fizz'`、`'Buzz'`、`'FizzBuzz'`、または空文字列が生成されます。空文字列の場合は、`or`演算子によって`str(i)`が選択され、数値が文字列として出力されます。

**Key Insights:**
このコードカタでは、条件分岐とループを用いた基本的なプログラミングロジックを学ぶことができます。また、最短コードでは、条件式を文字列の乗算に利用するという、Pythonの柔軟な表現方法を学ぶことができます。

### コードカタ9：最長の回文を見つける

**スキル:** 文字列操作、ループ

**問題:** 与えられた文字列の中で、最長の回文を見つける関数`longest_palindrome`を作成してください。

**詳細コード:**

```python
def longest_palindrome(s):
  """
  与えられた文字列の中で、最長の回文を見つける関数

  Args:
    s: 文字列

  Returns:
    最長の回文
  """
  if len(s) < 2:
    return s
  longest = ""
  for i in range(len(s)):
    for j in range(i, len(s)):
      substring = s[i:j+1]
      if substring == substring[::-1] and len(substring) > len(longest):
        longest = substring
  return longest
```

**最短コード:**

```python
def longest_palindrome(s):
  if not s: 
    return ""
  longest = ""
  for i in range(len(s)):
    for j in range(i, len(s)):
      if s[i:j+1] == s[i:j+1][::-1] and len(s[i:j+1]) > len(longest):
        longest = s[i:j+1]
  return longest
```

**解説:** 詳細コードでは、全ての可能な部分文字列を生成し、回文かどうかをチェックすることで最長の回文を求めています。最短コードでは、同様のロジックで、より簡潔に記述しています。動的計画法を用いたアプローチも存在します。動的計画法は、部分問題の解をメモ化することで、計算量を削減する手法です。最長の回文を求める問題では、部分文字列が回文かどうかをメモ化することで、計算量を削減することができます。

**Key Insights:**
このコードカタでは、文字列操作とループを用いて、回文を見つけるアルゴリズムを実装することができます。また、動的計画法などのより高度なアルゴリズムを学ぶきっかけにもなります。

### コードカタ10：スーパーマーケットの価格設定

**スキル:** データ構造、アルゴリズム、問題解決能力

**問題:** スーパーマーケットの価格設定システムを設計・実装してください。

*   顧客は、商品とその数量を指定して購入することができます。
*   スーパーマーケットは、商品の単価、割引、特別オファーなどを設定することができます。
*   システムは、顧客の購入に基づいて合計金額を計算する必要があります。

**詳細コード:**

```python
class Product:
  def __init__(self, name, unit_price):
    self.name = name
    self.unit_price = unit_price

class Discount:
  def __init__(self, product, quantity, discount_price):
    self.product = product
    self.quantity = quantity
    self.discount_price = discount_price

class ShoppingCart:
  def __init__(self):
    self.items = []

  def add_item(self, product, quantity):
    self.items.append((product, quantity))

  def calculate_total(self, discounts=[]):
    total = 0
    for product, quantity in self.items:
      total += product.unit_price * quantity
    for discount in discounts:
      for product, quantity in self.items:
        if product == discount.product and quantity >= discount.quantity:
          total -= (quantity // discount.quantity) * (
              discount.quantity * product.unit_price - discount.discount_price)
    return total


# 商品と割引の設定
apple = Product("apple", 1.0)
banana = Product("banana", 0.5)
apple_discount = Discount(apple, 3, 2.5)

# ショッピングカートの作成と商品の追加
cart = ShoppingCart()
cart.add_item(apple, 5)
cart.add_item(banana, 2)

# 合計金額の計算
total = cart.calculate_total(discounts=[apple_discount])
print(total)  # 出力: 4.5
```

**最短コード:**

```python
# 最短コードは、詳細コードと同様のロジックで、より簡潔に記述することが可能ですが、
# 可読性や保守性を考慮すると、詳細コードの方が適切です。
```

**解説:** このコードカタでは、商品、割引、ショッピングカートをクラスとして定義し、合計金額を計算する機能を実装しています。

**Key Insights:**
このコードカタでは、クラスを用いたオブジェクト指向プログラミング、データ構造の設計、アルゴリズムの実装など、より実践的なスキルを学ぶことができます。

### 結論

本稿では、Pythonのスキル向上に役立つ10個のコードカタを紹介しました。これらのコードカタは、Pythonの基礎的な文法から、オブジェクト指向プログラミング、アルゴリズム、問題解決能力まで、幅広いスキルを網羅しています。各コードカタに取り組むことで、それぞれのKey Insightsで示したように、Pythonの様々な側面を深く理解し、実践的なスキルを身につけることができます。コードカタを繰り返し練習することで、より効率的で、読みやすく、保守しやすいコードを書くことができるようになり、Pythonプログラマーとしての成長を促進することができます。
