# 🍒 さくらんぼ たしざん｜玉から暗算へ（試作 v2.0）

小学校低学年向け、ブラウザで使う10のまとまりの足し算教材です。タブレットの指操作に対応しています。ファイルは `index.html` の1つで動き、ライブラリの読み込みやアカウント登録は不要です。

## 何ができる？

画面上部に **元の足し算（例：8＋5＝？）を常に表示**しながら、次の段階で少しずつヒントを減らします。

1. **① たま**：青玉をワンタップ（またはドラッグ）して10の箱を完成させ、さくらんぼの数の分解を見て答えを選ぶ。
2. **② ず**：玉を動かさず、10マスの図を見て10まで必要な数を答え、続けて和を答える。必要なら空きマスを数えるヒント。
3. **③ しき**：最初は10マスを隠し、さくらんぼで「何と何に分ける？」を考え、和を答える。ヒントで10マスを表示できる。
4. **④ じぶん**：最初は式だけで計算し、選択肢ではなく数字キーで答える。困ったら10マス→さくらんぼの順に助けを出す。
5. **🌱 おさらい**：前に練習した問題、とくに間違えたりヒントを使った問題を優先して5問復習する。自力モードと同じ数字入力方式。

各通常モードは10問。正解すると次の問題へ。問題を間違えてもペナルティはありません。やり直し・段階の切り替えは自由です。

## 次の段階への移行

各段階の最後5問中、4問以上で「初回正解・ヒントなし」だった場合は、次の段階を**試す提案**が出ます。自動昇格・ロック・能力診断ではありません。これはアプリ内での暫定基準で、学術研究が裏付ける一律の合格ラインではありません。

大人がそばで「どうして8＋5が10＋3になる？」と聞き、子どもの説明を確かめることも大切です。玉なしで解けるかどうかは、**別の日や紙で初見の問題**を解いたときにも確認してください。

## GitHub Pagesに公開する手順

1. GitHubに新しいリポジトリを作成（例：`sakuranbo-learning`）。
2. このフォルダの `index.html`、`README.md`、`.nojekyll`、`QA.md` を直下に置いてコミット。
3. GitHubの `Settings → Pages → Build and deployment` で `Deploy from a branch`、`main`、`/(root)` を指定。
4. 生成された `https://<username>.github.io/<repository>/` にアクセス。
5. 娘さんのiPadのSafariで、①玉のワンタップ→②図→③式→④数字入力→おさらい→画面再読込後の記録まで試す。

既存のGitHub Pagesリポジトリを使う場合は `index.html` を新版に差し替えればよいです。GitHubへのアップロードや公開設定の変更はこのZIPだけでは行いません。

## 記録とプライバシー

- 記録項目：日付、出題した数字、モード、初回正解か、ヒント・誤答の有無。
- `localStorage` に最大300問分を保存。使うブラウザ・端末に依存し、消去されることがあります。
- 名前・写真・学校名・個人アカウントは取得しません。教材のJavaScriptに外部通信処理はありません。公開サーバーへの通常アクセス通信は別です。
- 親向け欄の「学習記録を消す」で履歴を消去できます。**削除は取り消せません**。

## 教育研究上の位置づけ

この教材は、具体物（玉）→図→式→支援なしへ進む設計です。具体物と数式を結びつけ、支援を段階的に減らす方向性は教育研究と整合していますが、**このアプリの成績改善や定着効果は未検証**です。

参考資料：
- Education Endowment Foundation, “Use manipulatives and representations to develop understanding” — https://educationendowmentfoundation.org.uk/early-years/maths/use-manipulatives-and-representations-to-develop-understanding/
- Fyfe et al. (2014), *Concreteness Fading in Mathematics and Science Instruction: A Systematic Review* — https://eric.ed.gov/?id=EJ1036777
- Fyfe et al. (2015), *Benefits of “concreteness fading” for children's mathematics understanding* — https://www.sciencedirect.com/science/article/pii/S0959475214000942
- NCETM, *Addition and subtraction: bridging 10* — https://www.ncetm.org.uk/teaching-for-mastery/mastery-materials/primary-mastery-professional-development/number-addition-and-subtraction/
