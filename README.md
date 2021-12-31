# myKotlinNote
Kotlinの書き方まとめ

## 変数の定義

- `val`と`var`がある

```
val a = 1       // 値などの指定は1回のみ
a = 2           // Error

var b = 3       // 値などの指定は何回でも良い
b = 4
```

## コレクション`List`

- Listは2種類ある
- 変更不可`listOf`
- 変更可能`mutableListOf`

```
val logs = mutableListOf<Int>(100)  // 初期値があれば型指定は不要
logs.add(200)                       // 要素を追加できる
println(logs)                       // [100, 200]
println(logs.size)                  // 2, コレクションの大きさが分かる
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