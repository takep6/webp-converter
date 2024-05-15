
# 画像圧縮変換ツール　アッシュくん

画像生成AIで作られたプロンプト付き画像を、プロンプトを消さずに圧縮変換できるツールです。<br>
プロンプトが含まれていない画像でも、対応するファイル形式であれば変換できます。<br>
png, jpg, webp, avif形式に対応しています。<br><br>

#### ※注意
Stable Diffusion web UIなどで生成した画像にのみ対応しています。<br>
NovelAI等のクラウドサービスで生成された画像のプロンプトは保存されません。プロンプト以外のメタデータも保存されません（変換処理はされます）。<br>
<br>
アニメーションファイルや上記のファイル形式以外のファイルも非対応です。<br>
非対応のファイルは変換せずにスルーしてしまうので、変換前後でファイル数に違いがないか確認をおすすめします。
<br><br>

## 推奨環境
Windows10, 11<br>
Python3.8以上<br><br>

## 導入方法
方法①（簡単）：<br>
<b>run.bat</b> を実行してください。<br>
自動で仮想環境を作成してモジュールをインストールした後、アプリを起動します。
<br><br>

方法②（わかる人向け）：<br>
コマンドプロンプトから以下のコードを実行してください。<br>
```
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python main.py
```
<br>

## 起動方法
方法①：<br>
<b>run.bat</b> を実行するとアプリが起動します。
<br><br>

方法②：<br>
```
python main.py
```
上記のスクリプトを実行してください。
<br><br>


## 使い方
<img width="400" alt="screenshot" src="https://github.com/takep6/image-converter-with-prompt/assets/74190436/e32ca137-2339-464d-8a5d-4a6b9aaddb25">
<br><br>

#### 入力フォルダパス：
変換したい画像のファイルパス、または画像の入ったフォルダを指定します。
<br><br>

#### 出力フォルダパス：
変換後の画像を保存するフォルダパスを指定します。<br>
フォルダが存在しない場合は新しく作成されます。
<br><br>

#### 変換後の拡張子：
出力する画像の画像形式を決定します。<br>
png, jpg, webp, avif から選択できます。
<br><br>

#### 可逆圧縮モード：
画質を劣化させずに圧縮（lossless）するかどうかを選択します。<br>
"変換後の拡張子" でpngを選ぶと自動でONに、jpg, avifを選ぶと自動でOFFになります。webpはON/OFFを選択できます。
<br><br>

#### 品質：
画像の圧縮率を決めます。値が高いほど元の画像に近い画質になりますが、ファイルサイズが大きくなります。<br>
可逆圧縮モードがOFFの場合のみ適用されます。
<br><br>

#### 透過部分を塗りつぶす：
透明な部分がある画像（主にpng, webp, avif）の透過部分を一色で塗りつぶすかどうか決めます。
<br><br>

#### 透明部分の色：
透明な部分を選択した色で一色に塗りつぶします。<br>
"透過部分を塗りつぶす" がONの場合のみ適用されます。
<br><br>

#### 実行ボタン：
変換処理を実行します。
<br><br>

#### 停止ボタン：
変換処理を途中で終了します。
<br><br>

#### 設定アイコンボタン：
サイドメニューを開きます。
<br><br>

#### 同時プロセス実行数：
画像変換処理を同時に実行する最大数を決めます。<br>
画像の枚数が多い場合は値を大きくした方が、処理時間を短縮できます。
<br><br>

#### テーマ：
ライトテーマ/ダークテーマを切り替えます。
<br><br>

## ライセンス
このプロジェクトは [AGPL-3.0 license](LICENSE.txt) ライセンスの元にライセンスされています。
<br><br>

## 謝辞
[stable-diffusion-webui（AUTOMATIC1111氏）](https://github.com/AUTOMATIC1111/stable-diffusion-webui)<br>
[stable-diffusion-webui-forge（lllyasviel氏）](https://github.com/lllyasviel/stable-diffusion-webui-forge)
<br><br>
アプリを製作するにあたって一部のコードを使用させていただきました。感謝いたします。






