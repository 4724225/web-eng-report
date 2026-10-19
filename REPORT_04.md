# 第4回 Webエンジニアリング演習 レポート
## 学籍番号
4724225
## `const`と`let`の宣言・再代入に使用したコード
const courseName = "Web Engineering";
let retryCount = 1;
courseName = "Other Course"; // エラー確認後に削除する
retryCount = 2;
## VSCodeと`pnpm run check`に表示されたエラー番号・メッセージ
src/index.ts:3:1 - error TS2588: Cannot assign to 'courseName' because it is a constant.

3 courseName = "Other Course"; // エラー確認後に削除する
  ~~~~~~~~~~


Found 1 error in src/index.ts:3
## 修正後の実行結果と`const`・`let`の違いの説明
$ tsx src/index.ts
Course Name: Web Engineering, Retry Count: 2

constは変数名への再代入ができない
letは再代入ができるため後から値を入れ替えられる