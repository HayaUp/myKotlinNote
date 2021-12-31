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