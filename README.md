# myKotlinNote
Kotlinの書き方まとめ

## 変数の定義

- `val`と`var`がある

```Kotlin
val a = 1       // 値などの指定は1回のみ
a = 2           // Error

var b = 3       // 値などの指定は何回でも良い
b = 4
```

## 文字列型`String`

### 区切り文字による分割

```Kotlin
val text = "123 456 789"
val textArray = text.split(" "))        // List<String>
println(textArray)                      // [123, 456, 789]
```

### 区切り文字による連結

```Kotlin
val textArray = listOf("123", "456", "789")
val text = textArray.joinToString("/")
println(text)                                   // "123/456/789"
```

### 文字列検索

```Kotlin
val text = "aAbBcC"
println(text.indexOf("a"))      // 0
println(text.indexOf("A"))      // 1
println(text.indexOf("c"))      // 4
println(text.indexOf("C"))      // 5
println(text.indexOf("Z"))      // -1
```

### 指定した文字列を含むか

```Kotlin
val text = "aAbBcC"
println(text.contains("b"))     // true
println(text.contains("bB"))    // true
println(text.contains("Z"))     // false
```

## コレクション`List`

- Listは2種類ある
- 変更不可`listOf`
- 変更可能`mutableListOf`

```Kotlin
val logs = mutableListOf<Int>(100)  // 初期値があれば型指定は不要
logs.add(200)                       // 要素を追加できる
println(logs)                       // [100, 200]
println(logs.size)                  // 2, コレクションの大きさが分かる
```

### 反復

- `for`と`forEach`がある

```Kotlin
val nList = listOf(100, 200, 300)

for (element in nList) {
    println(element)
}

nList.forEach {
    println(it)
}
```

- forEach に index を使いたい場合

```Kotlin
val nList = listOf(100, 200, 300)

nList.forEachIndexed {index, value -> println("[$index] = $value")}
```

## 文字列の操作

### 区切り文字による分割

```Kotlin
val message = "123 456 789"
val words = message.split(" ")      // split の第一引数に区切り文字を指定する
println(words)                      // [123, 456, 789]
```

### コレクションの要素を区切り文字で連結

```Kotlin
val words = listOf(1, 2, 3)
val message = words.joinToString("/")
println(message)                            // 1/2/3
```