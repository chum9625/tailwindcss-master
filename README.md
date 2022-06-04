# Tailwind CSS set up flow

公式サイト：[Get started with  Tailwind CSS](https://tailwindcss.com/docs/installation)

## インストールの種類

1. Tailwind CLI
2. Using PostCSS
3. Framework Guides
4. Play CDN

💡 今回は [2](https://tailwindcss.com/docs/installation/using-postcss) で進める。  
🙅 4 は非推奨。試用時のみに留める。

## 手順

📗 Tailwind CSS を PostCSSのプラグインとして使う手順

1. ` npm init -y`  👉 package.json の生成
2. ` npm install -D tailwindcss postcss autoprefixer `
3. ` npm uninstall postcss ` 👉 postcss-cli に変更する
4. ` npm i -D postcss-cli ` 👉 npm run build コマンド使用可能
5. ` npx tailwindcss init -p`  👉 設定ファイル作成。 -p オプションはPostCSS構成ファイルの作成: postcss.config.js
6. コンパイルされたcssを出力するためのdistフォルダとコンパイル前のcssを入れておくためのsrcフォルダを作成する。
   💡 フォルダ構成
   ` 
   ``  ├dist`
   ``  ├node_modules
   `  ├package-lock.json
   `  ├package.json
   `  ├src
   `
7. tailwind.config.jsにディレクトリを指定。
8. input.css（名前は自由）を作成。
9. 公式サイトからTailwindディレクティブをinput.cssにコピペ。
10. VScode拡張機能 PostCSS Language Support を追加。（インストール済ならskip）
11. index.html を作成し、スタイルシート /dist/output.css 読込及び作成する。
   💡 distという名前はビルド後のファイルによく付けられる。
12. VScode拡張機能 Tailwind CSS IntelliSense を追加。
   💡 補完効かない場合は設定項目追記：` "editor.quickSuggestions": {"strings": true } `

13. package.json の "scripts" にbuildコマンドを追記する。
14. ` npm run build `
15. npm run dev 開発環境を作る
