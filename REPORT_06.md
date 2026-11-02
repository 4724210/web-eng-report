# 第6回 Webエンジニアリング演習 レポート
## 学籍番号
4724210
## `Todo`型の定義
export type Todo = {
  id: number;
  title: string;
  completed: boolean;
  dueDate?: string;
};

## 未完了件数を返す関数の引数と戻り値の型
export async function collectTodo(): Promise<number> {
    const currentTodos = await fetchTodos();
    const incompleteTodos = currentTodos.filter(
        (todo) => !todo.completed,
    );
    return incompleteTodos.length;
}
## 未完了件数の実行結果
[
  { id: 1, title: '型を復習する', completed: true },
  { id: 2, title: '配列を学ぶ', completed: true },
  { id: 3, title: 'レポートを書く', completed: false },
  { id: 4, title: '提出する', completed: false }
]
2
