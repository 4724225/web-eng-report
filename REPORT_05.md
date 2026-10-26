# 第5回 Webエンジニアリング演習 レポート
## 学籍番号
4724225
## TODO配列のコード
const todos = [
    { id: 1, title: "型を復習する", completed: true },
    { id: 2, title: "配列を学ぶ", completed: false },
    { id: 3, title: "レポートを書く", completed: true },
    { id: 4, title: "提出する", completed: true },
];
## TODOを更新した条件
const completedBefore = todos.filter((todo) => todo.completed).length;

for (const todo of todos) {
    if (todo.id === 2) {
        todo.completed = true;
        console.log(`更新後: ${todo.title} [完了]`);
    }
}

const completedAfter = todos.filter((todo) => todo.completed).length;
console.log(`完了件数: 更新前 ${completedBefore}件 -> 更新後 ${completedAfter}件`);

## 完了件数の更新前後の実行結果
[更新前]
$ tsx src/index.ts
ID: 1, タイトル: 型を復習する, ステータス: 完了
ID: 2, タイトル: 配列を学ぶ, ステータス: 未完了
ID: 3, タイトル: レポートを書く, ステータス: 完了
ID: 4, タイトル: 提出する, ステータス: 完了
3

[更新後]
更新後: 配列を学ぶ [完了]
完了件数: 更新前 3件 -> 更新後 4件
ID: 1, タイトル: 型を復習する, ステータス: 完了
ID: 2, タイトル: 配列を学ぶ, ステータス: 完了
ID: 3, タイトル: レポートを書く, ステータス: 完了
ID: 4, タイトル: 提出する, ステータス: 完了
4