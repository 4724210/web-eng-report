# 第4回 Webエンジニアリング演習 レポート
## 学籍番号
4724210
## `const`と`let`の宣言・再代入に使用したコード
const courseName = "Web Engineering"
let retryCount = 1 

courseName="mojiretsu"
retryCount = 2
## VSCodeと`pnpm run check`に表示されたエラー番号・メッセージ
定数であるため、'courseName'に代入することはできません。 ts(2588)

$ tsc --noEmit src/index.ts
src/index.ts:23:1 - error TS2588: Cannot assign to 'courseName' because it is a constant.

23 courseName="mojiretsu"
   ~~~~~~~~~~


Found 1 error in src/index.ts:23
## 修正後の実行結果と`const`・`let`の違いの説明
Web Engineering 2
constは変数名への再代入ができないが、letは値を再代入することが可能
