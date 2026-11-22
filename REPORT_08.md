# 第8回 Webエンジニアリング演習 レポート
## 学籍番号
4724225
## コンポーネント構成
〇`App` (`src/App.tsx`): 全体のレイアウトとTODO配列データの保持を担当し、`TodoList` へデータを渡す。
`TodoList` (`src/components/〇TodoList.tsx`): `todos` 配列を `map` で展開し、各要素を `TodoItem` として一覧表示する。
〇`TodoItem` (`src/components/TodoItem.tsx`): 1件の `todo` データをPropsとして受け取り、タイトル・完了状態・期限（設定時のみ）を表示する。
## `TodoItem`のProps型
type TodoItemProps = {
  todo: Todo;
};
## 期限あり・なしの画面確認結果
Reactを学ぶ (完了)
Propsを確認する (未完了) (期限: 2025-01-01)
Stateを更新する (未完了