# 第9回 Webエンジニアリング演習 レポート
## 学籍番号
4724225
## Stateの一覧と役割
title:入力中の文字列を保持する
todo:画面に表示するTODOオブジェクトの配列を保持する
## 完了ボタンから画面更新まで
（呼ばれる関数、Stateの持ち主、Propsとの関係）
## 空白入力を防ぐコードと確認結果
function handleSubmit(event: SubmitEvent<HTMLFormElement>) {
  event.preventDefault();
  const normalizedTitle: string = title.trim();
  if (normalizedTitle === "") {
    return;
  }
  const newTodo: Todo = {
    id: Date.now(),
    title: normalizedTitle,
    completed: false,
  };
  setTodos((current) => [...current, newTodo]);
  setTitle("");
}

空文字のまま送信：一覧の件数が変わらないことを確認

半角スペース3文字を送信：一覧の件数が変わらないことを確認

前後に空白を入れて文字を入力して送信：前後の空白が取り除かれ、1件追加されることを確認

文字入力しEnterで送信：1件追加され、入力欄が空になるのを確認

完了ボタン：クリックで完了・未完了が切り替わることを確