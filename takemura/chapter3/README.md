# 3章 型推論と制御フロー解析

静的な型付け（型アノテーション、静的型）と明示的な型付け（型推論）を分けること。これまで見てきた通り、人間よりコンパイラやリンターの方が賢い。

## 項目18

- [3-1.ts](https://github.com/chaploud/EffectiveTypeScript/blob/main/takemura/chapter3/3-1.ts) ちょっと思ってるのと挙動が違ったので。デフォルト値ある場合は型指定はいらなさそう

- [3-2.ts](https://github.com/chaploud/EffectiveTypeScript/blob/main/takemura/chapter3/3-2.ts) 本の思想的に、オブジェクトの型を使いまわしたいときは理由がないときは `typeof` のような使い方をしなさいと言っているように感じる。

結局typeやinterfaceで型を付けるのは、人間によるアノテーションと変わらないため…


## 項目19

コンパイラの都合や歴史的経緯によって、変数の型は途中で変わらない方が一般に読みやすい。

## 項目20

p112: readonlyは浅くreadonlyを適用するが、`as const`は深くreadonlyを適用する。

`satisfies` や `as const` は関数の戻り値や引数では使えない。

```TypeScript
type Point = [number, number];
function apiCall(params: Record<string, string|number>) : T satisfies Record<string, Point>; // NG
function getSquare(p1: Point as const, p2: Point as const): number; // NG
```