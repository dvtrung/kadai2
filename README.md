# 工学部専門科目「プログラミング言語」(2016年度)

## 課題2 (締切 1/9 (月) 23:59)

__計算木__ とは以下のような2分木の一種である．

* 葉 (`leaf`) は計算木である．ただし，葉には正整数が格納されている．
* ふたつの計算木 t1 と t2 に対し，枝 (`branch(t1, t2)`) は計算木である．ただし，枝にはタイプSの枝とタイプMの枝の二種類がある．

この時，枝の価値を以下のように定義する．

* 葉の価値は，格納された整数値そのものである．
* 枝の価値は，タイプSの枝の場合は部分木の価値の和，タイプMの枝の場合は部分木の価値の積である．

### 課題2-1

C言語で計算木のデータ構造を構造体を使って定義し(名前は `tree` とせよ)，価値を計算するための関数 `int value(struct tree*)` を定義せよ．

### 課題2-2(オプション)

課題2-1のプログラムを元にして，計算木の価値を表す計算式を表示する関数 `print_tree` を定義せよ．(C言語での文字列の取り扱いについては教えていないので，文字列を返す関数は定義しなくてよく，`printf` を使って表示するだけでよい．)

注意: 単に木の価値を計算してからその結果(この例であれば `"3"`) を答えとするのは認めない．(つまり，葉に格納された数値は全て文字列に含まれるようにせよ．)

### 課題2-3(オプション)

課題2-2のプログラムを元にし，`printf` を使って括弧を適宜省いた文字列を表示するような関数 `print_tree_fewer_parens` を定義せよ．結合については課題1-4と同様である．

### 課題1-5(オプション)

課題2-1のプログラムを元にして，課題1-5と同様な「木の簡約操作」を行うような関数 `struct tree *reduce(struct tree *)` を定義せよ．

> 簡約操作: ふたつの葉を部分木として持つ枝一箇所を適当に選んで，その部分木を，その部分木の価値を格納した葉で置換する．木に該当箇所がひとつもない場合には，入力された木がそのまま出力となる．


## プログラム作成上の注意

* 単にメソッドや関数の定義を与えるだけでなく，それがうまく動くことを確認するコードをつけること．2分探索木のそれを参考にしてほしい．
* コンパイルができないプログラムを提出した場合には採点の対象外となる．

## 提出要領

1. https://github.com/ProgrammingLanguages2016AtKUEng/kadai2 からファイルをダウンロードする．(git 使いはもちろん clone してもよい．) 
2. C プログラムは `C` フォルダに入れること．
3. プログラムの説明を __課題毎に__ つけること．フォーマットは自由だが内容だけでなく読みやすさも採点の対象となる．これは，この `README.md` と同じフォルダに置くこと．
4. プログラムの説明を入れたフォルダを圧縮して zip ファイルを作り，PandA で提出すること．GitHub 使いで GitHub 経由の提出の実験~~の人柱になる~~に協力してくれる人がいると嬉しいです(以下を参照のこと)．

### GitHub 使いの人へ

1. 課題レポジトリの作成をする．https://classroom.github.com/assignment-invitations/fe397d97cf13a3c2022ae2937e31f3ac にアクセスし，手続を進めると，`kadai2-〈GitHubアカウント〉` という名前のレポジトリが生成される．(これは上の レポジトリと同内容のはずです．)
1. このレポジトリを fork，自分の PC に clone する．
1. ブランチを作って(名前はなんでもよいです)，課題に沿って編集して commit, GitHub へ push する．
1. Fork 元にプルリクを出したら提出完了．


