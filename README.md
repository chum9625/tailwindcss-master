# Tailwind CSS set up flow

公式サイト：[Get started with  Tailwind CSS](https://tailwindcss.com/docs/installation)

## インストールの種類

1. Tailwind CLI
2. Using PostCSS
3. Framework Guides
4. Play CDN

💡 今回は [2](https://tailwindcss.com/docs/installation/using-postcss) で進める。  
🙅 4 は非推奨。試用時のみに留める。（CSSに制限があるため）

## 手順 📗 Tailwind CSS を PostCSSのプラグインとして使う

1. ` npm init -y`  👉 package.json の生成
2. ` npm install -D tailwindcss postcss-cli autoprefixer `
3. ` npm i -D postcss-cli ` 👉 npm run build コマンド使用可能
4. ` npm i -D cssnano ` 👉 build実行時に cssを minify化 
5. ` npx tailwindcss init -p`  👉 設定ファイル作成。 -p オプションはPostCSS構成ファイルの作成: postcss.config.js
6. コンパイルされたcssを出力するためのdistフォルダとコンパイル前のcssを入れておくためのsrcフォルダを作成する。  

   💡 フォルダ構成  
          ├ dist  
          ├ node_modules  
          ├ package-lock.json  
          ├ package.json  
          └ src  

6. tailwind.config.jsの設定。（` jit`  と読込ディレクトリ指定）
7. input.css（名前は自由）を作成。
8. 公式サイトからTailwindディレクティブをinput.cssにコピペ。
9. index.html を作成、head内にスタイルシート（../dist/output.css）読込及びoutput.cssを作成。  
   💡 distという名前はビルド後のファイルによく付けられる。
10. VScode拡張機能 **PostCSS Language Support** を追加。（インストール済ならskip）
11. VScode拡張機能 Tailwind CSS IntelliSense を追加。  
   💡 補完効かない場合は設定項目追記：` "editor.quickSuggestions": {"strings": true } `
12. postcss.config.js でCSS圧縮（cssnano）の設定をする。
13. package.json の "scripts" に実行コマンドを追記する。
    1.  ` npm run dev ` （開発用 - watch追加、CSS圧縮無し）
    2.  ` npm run build ` （公開用 - CSS圧縮有り）

## Tailwind CSS Docs

- [TailwindCSS](https://tailwindcss.com/docs/installation)
- [TailwindCSS JP](https://tailwindcss.jp/docs/installation)
- [daisyUI](https://daisyui.com/components/)
- [Flowrift](https://flowrift.com/w/)
- [CHEAT SHEET](https://nerdcave.com/tailwind-cheat-sheet)
