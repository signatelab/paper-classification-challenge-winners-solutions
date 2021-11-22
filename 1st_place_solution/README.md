<!DOCTYPE html>
<html>
<head>
<!-- <title>README.md</title>
<meta http-equiv="Content-type" content="text/html;charset=UTF-8"> -->

<!-- <style>
/* https://github.com/microsoft/vscode/blob/master/extensions/markdown-language-features/media/markdown.css */
/*---------------------------------------------------------------------------------------------
 *  Copyright (c) Microsoft Corporation. All rights reserved.
 *  Licensed under the MIT License. See License.txt in the project root for license information.
 *--------------------------------------------------------------------------------------------*/

body {
	font-family: var(--vscode-markdown-font-family, -apple-system, BlinkMacSystemFont, "Segoe WPC", "Segoe UI", "Ubuntu", "Droid Sans", sans-serif);
	font-size: var(--vscode-markdown-font-size, 14px);
	padding: 0 26px;
	line-height: var(--vscode-markdown-line-height, 22px);
	word-wrap: break-word;
}

#code-csp-warning {
	position: fixed;
	top: 0;
	right: 0;
	color: white;
	margin: 16px;
	text-align: center;
	font-size: 12px;
	font-family: sans-serif;
	background-color:#444444;
	cursor: pointer;
	padding: 6px;
	box-shadow: 1px 1px 1px rgba(0,0,0,.25);
}

#code-csp-warning:hover {
	text-decoration: none;
	background-color:#007acc;
	box-shadow: 2px 2px 2px rgba(0,0,0,.25);
}

body.scrollBeyondLastLine {
	margin-bottom: calc(100vh - 22px);
}

body.showEditorSelection .code-line {
	position: relative;
}

body.showEditorSelection .code-active-line:before,
body.showEditorSelection .code-line:hover:before {
	content: "";
	display: block;
	position: absolute;
	top: 0;
	left: -12px;
	height: 100%;
}

body.showEditorSelection li.code-active-line:before,
body.showEditorSelection li.code-line:hover:before {
	left: -30px;
}

.vscode-light.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(0, 0, 0, 0.15);
}

.vscode-light.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(0, 0, 0, 0.40);
}

.vscode-light.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

.vscode-dark.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(255, 255, 255, 0.4);
}

.vscode-dark.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(255, 255, 255, 0.60);
}

.vscode-dark.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

.vscode-high-contrast.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(255, 160, 0, 0.7);
}

.vscode-high-contrast.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(255, 160, 0, 1);
}

.vscode-high-contrast.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

img {
	max-width: 100%;
	max-height: 100%;
}

a {
	text-decoration: none;
}

a:hover {
	text-decoration: underline;
}

a:focus,
input:focus,
select:focus,
textarea:focus {
	outline: 1px solid -webkit-focus-ring-color;
	outline-offset: -1px;
}

hr {
	border: 0;
	height: 2px;
	border-bottom: 2px solid;
}

h1 {
	padding-bottom: 0.3em;
	line-height: 1.2;
	border-bottom-width: 1px;
	border-bottom-style: solid;
}

h1, h2, h3 {
	font-weight: normal;
}

table {
	border-collapse: collapse;
}

table > thead > tr > th {
	text-align: left;
	border-bottom: 1px solid;
}

table > thead > tr > th,
table > thead > tr > td,
table > tbody > tr > th,
table > tbody > tr > td {
	padding: 5px 10px;
}

table > tbody > tr + tr > td {
	border-top: 1px solid;
}

blockquote {
	margin: 0 7px 0 5px;
	padding: 0 16px 0 10px;
	border-left-width: 5px;
	border-left-style: solid;
}

code {
	font-family: Menlo, Monaco, Consolas, "Droid Sans Mono", "Courier New", monospace, "Droid Sans Fallback";
	font-size: 1em;
	line-height: 1.357em;
}

body.wordWrap pre {
	white-space: pre-wrap;
}

pre:not(.hljs),
pre.hljs code > div {
	padding: 16px;
	border-radius: 3px;
	overflow: auto;
}

pre code {
	color: var(--vscode-editor-foreground);
	tab-size: 4;
}

/** Theming */

.vscode-light pre {
	background-color: rgba(220, 220, 220, 0.4);
}

.vscode-dark pre {
	background-color: rgba(10, 10, 10, 0.4);
}

.vscode-high-contrast pre {
	background-color: rgb(0, 0, 0);
}

.vscode-high-contrast h1 {
	border-color: rgb(0, 0, 0);
}

.vscode-light table > thead > tr > th {
	border-color: rgba(0, 0, 0, 0.69);
}

.vscode-dark table > thead > tr > th {
	border-color: rgba(255, 255, 255, 0.69);
}

.vscode-light h1,
.vscode-light hr,
.vscode-light table > tbody > tr + tr > td {
	border-color: rgba(0, 0, 0, 0.18);
}

.vscode-dark h1,
.vscode-dark hr,
.vscode-dark table > tbody > tr + tr > td {
	border-color: rgba(255, 255, 255, 0.18);
}

</style>

<style>
/* Tomorrow Theme */
/* http://jmblog.github.com/color-themes-for-google-code-highlightjs */
/* Original theme - https://github.com/chriskempson/tomorrow-theme */

/* Tomorrow Comment */
.hljs-comment,
.hljs-quote {
	color: #8e908c;
}

/* Tomorrow Red */
.hljs-variable,
.hljs-template-variable,
.hljs-tag,
.hljs-name,
.hljs-selector-id,
.hljs-selector-class,
.hljs-regexp,
.hljs-deletion {
	color: #c82829;
}

/* Tomorrow Orange */
.hljs-number,
.hljs-built_in,
.hljs-builtin-name,
.hljs-literal,
.hljs-type,
.hljs-params,
.hljs-meta,
.hljs-link {
	color: #f5871f;
}

/* Tomorrow Yellow */
.hljs-attribute {
	color: #eab700;
}

/* Tomorrow Green */
.hljs-string,
.hljs-symbol,
.hljs-bullet,
.hljs-addition {
	color: #718c00;
}

/* Tomorrow Blue */
.hljs-title,
.hljs-section {
	color: #4271ae;
}

/* Tomorrow Purple */
.hljs-keyword,
.hljs-selector-tag {
	color: #8959a8;
}

.hljs {
	display: block;
	overflow-x: auto;
	color: #4d4d4c;
	padding: 0.5em;
}

.hljs-emphasis {
	font-style: italic;
}

.hljs-strong {
	font-weight: bold;
}
</style> -->

<!-- <style>
/*
 * Markdown PDF CSS
 */

 body {
	font-family: -apple-system, BlinkMacSystemFont, "Segoe WPC", "Segoe UI", "Ubuntu", "Droid Sans", sans-serif, "Meiryo";
	padding: 0 12px;
}

pre {
	background-color: #f8f8f8;
	border: 1px solid #cccccc;
	border-radius: 3px;
	overflow-x: auto;
	white-space: pre-wrap;
	overflow-wrap: break-word;
}

pre:not(.hljs) {
	padding: 23px;
	line-height: 19px;
}

blockquote {
	background: rgba(127, 127, 127, 0.1);
	border-color: rgba(0, 122, 204, 0.5);
}

.emoji {
	height: 1.4em;
}

code {
	font-size: 14px;
	line-height: 19px;
}

/* for inline code */
:not(pre):not(.hljs) > code {
	color: #C9AE75; /* Change the old color so it seems less like an error */
	font-size: inherit;
}

/* Page Break : use <div class="page"/> to insert page break
-------------------------------------------------------- */
.page {
	page-break-after: always;
}

</style> -->

<!-- <script src="https://unpkg.com/mermaid/dist/mermaid.min.js"></script>
</head>
<body>
  <script>
    mermaid.initialize({
      startOnLoad: true,
      theme: document.body.classList.contains('vscode-dark') || document.body.classList.contains('vscode-high-contrast')
          ? 'dark'
          : 'default'
    });
  </script> -->
<h1 id="readme">README</h1>
<h2 id="%E5%AE%9F%E9%A8%93%E7%92%B0%E5%A2%83">実験環境</h2>
<p>Google ColabのTPU v2を使って学習および予測を行うことを想定しています。</p>
<h2 id="%E3%83%87%E3%82%A3%E3%83%AC%E3%82%AF%E3%83%88%E3%83%AA%E6%A7%8B%E6%88%90">ディレクトリ構成</h2>
<p>Google Colab上に以下のようにファイルを配置してください。</p>
<pre class="hljs"><code><div>/content/drive/
└── MyDrive
        ├── Colab Notebooks
        │       └── SRWS-PSG-TF_提出用.ipynb
        ├── SRWS-PSG
        │       ├── config
        │       │       ├── test
        │       │       ├── train
        |       |       ├── ensemble.yml
        |       |       └── requirements.txt
        │       ├── sample_submit.csv
        |       ├── test.csv
        |       └── train.csv
        ├── experiments
        |       ├── 2021-09-08_000518
        |       |       ├── graphs
        |       |       ├── models
        |       |       ├── experiment.log
        |       |       └── oof_test.csv
        |       ├── 2021-09-11_043111
        |       ├── 2021-09-12_162335
        |       ├── 2021-09-21_120653
        |       ├── 2021-09-21_235528
        |       └── submission.csv
        └── cache
</div></code></pre>
<table>
<thead>
<tr>
<th style="text-align:left">File or dir name</th>
<th style="text-align:left">Memo</th>
<th style="text-align:center">自動生成</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">SRWS-PSG-TF_提出用.ipynb</td>
<td style="text-align:left">再現用ノートブック</td>
<td style="text-align:center"></td>
</tr>
<tr>
<td style="text-align:left">SRWS-PSG/</td>
<td style="text-align:left">train_data, test_data、設定ファイルを格納している</td>
<td style="text-align:center"></td>
</tr>
<tr>
<td style="text-align:left">SRWS-PSG/test/</td>
<td style="text-align:left">テストデータ予測用の設定ファイルを格納している</td>
<td style="text-align:center"></td>
</tr>
<tr>
<td style="text-align:left">SRWS-PSG/train/</td>
<td style="text-align:left">学習用の設定ファイルを格納している</td>
<td style="text-align:center"></td>
</tr>
<tr>
<td style="text-align:left">SRWS-PSG/ensemble.yml</td>
<td style="text-align:left">アンサンブル用の設定ファイル</td>
<td style="text-align:center"></td>
</tr>
<tr>
<td style="text-align:left">SRWS-PSG/requirements.txt</td>
<td style="text-align:left">パッケージインストール用</td>
<td style="text-align:center"></td>
</tr>
<tr>
<td style="text-align:left">experiments/{date}/graphs</td>
<td style="text-align:left">trainを実行するとlossの変化を表すグラフが格納される</td>
<td style="text-align:center">〇</td>
</tr>
<tr>
<td style="text-align:left">experiments/{date}/models</td>
<td style="text-align:left">trainを実行すると学習済みモデルが格納される。predict時には格納されたモデルがロードされる</td>
<td style="text-align:center">〇</td>
</tr>
<tr>
<td style="text-align:left">experiments/{date}/experiment.log</td>
<td style="text-align:left">train実行時に学習結果が記録される</td>
<td style="text-align:center">〇</td>
</tr>
<tr>
<td style="text-align:left">experiments/{date}/oof_test.csv</td>
<td style="text-align:left">test_dataの予測結果。predictを実行すると生成される</td>
<td style="text-align:center">〇</td>
</tr>
<tr>
<td style="text-align:left">experiments/submission.csv</td>
<td style="text-align:left">最終サブミッションファイル。ensembleを実行すると生成される</td>
<td style="text-align:center">〇</td>
</tr>
<tr>
<td style="text-align:left">cache</td>
<td style="text-align:left">Huggingface Transformersのcache directory</td>
<td style="text-align:center">〇</td>
</tr>
</tbody>
</table>
<h2 id="%E6%9C%80%E7%B5%82%E3%82%B5%E3%83%96%E3%83%9F%E3%83%83%E3%83%88%E5%86%8D%E7%8F%BE%E6%96%B9%E6%B3%95">最終サブミット再現方法</h2>
<ol>
<li>
<p><code>experiments/{date}/models</code>に学習済みモデルを配置します。</p>
</li>
<li>
<p>ノートブックを開き、Parametersセクションの<code>config_path</code>を以下のように書き換えます。</p>
<pre class="hljs"><code><div>config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/test/2021-09-21_235528.yml'</span>
</div></code></pre>
</li>
<li>
<p>すべてのセルを実行します。</p>
</li>
<li>
<p><code>experiments/2021-09-21_235528/oof_test.csv</code>が作成されていることを確認します。</p>
</li>
<li>
<p>以下のファイルについても同様に実行します。</p>
<pre class="hljs"><code><div>config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/test/2021-09-11_043111.yml'</span>
config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/test/2021-09-12_162335.yml'</span>
config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/test/2021-09-21_120653.yml'</span>
config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/test/2021-09-21_235528.yml'</span>
</div></code></pre>
</li>
<li>
<p>すべてのdateにおいて<code>experiments/{date}/oof_test.csv</code>が作成されていることを確認します。</p>
</li>
<li>
<p><code>config_path</code>を以下のように書き換えます。</p>
<pre class="hljs"><code><div>config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/ensemble.yml'</span>
</div></code></pre>
</li>
<li>
<p>すべてのセルを実行します。</p>
</li>
<li>
<p><code>experiments/submission.csv</code>が作成されます。</p>
</li>
</ol>
<h2 id="%E5%AD%A6%E7%BF%92%E6%96%B9%E6%B3%95">学習方法</h2>
<ol>
<li>
<p><code>experiments/{date}/models</code>にモデルファイルがある場合はバックアップを取っておきます。</p>
</li>
<li>
<p><code>config_path</code>を以下のように書き換えます。</p>
<pre class="hljs"><code><div>config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/train/2021-09-21_235528.yml'</span>
</div></code></pre>
</li>
<li>
<p>すべてのセルを実行します。</p>
</li>
<li>
<p>以下のファイルについても同様です。</p>
<pre class="hljs"><code><div>config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/train/2021-09-11_043111.yml'</span>
config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/train/2021-09-12_162335.yml'</span>
config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/train/2021-09-21_120653.yml'</span>
config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/train/2021-09-21_235528.yml'</span>
</div></code></pre>
</li>
<li>
<p>Utilsセクションの<code>read_threshold()</code>関数に<code>experiments/{date}/experiment.log</code>のファイルパスを与えると、thresholdを計算できます。</p>
</li>
</ol>
<h2 id="%E5%89%8D%E5%87%A6%E7%90%86%E3%83%87%E3%83%BC%E3%82%BF%E5%8F%96%E5%BE%97%E6%96%B9%E6%B3%95tfdatadataset%E5%BD%A2%E5%BC%8F">前処理データ取得方法（tf.data.Dataset形式）</h2>
<pre class="hljs"><code><div>config_path = <span class="hljs-string">'/content/drive/MyDrive/SRWS-PSG/config/train/2021-09-21_235528.yml'</span>
args = OmegaConf.load(config_path)

logger = create_logger(args.save_dir)
df_train, df_test = read_data(args)
data_provider = DataProvider(df_train, df_test, args)

<span class="hljs-comment"># 0 fold目の学習データを取得</span>
dataset = data_provider.create_train_dataset(fold=<span class="hljs-number">0</span>)
</div></code></pre>
<h2 id="%E3%83%91%E3%83%A9%E3%83%A1%E3%83%BC%E3%82%BF%E4%B8%80%E8%A6%A7">パラメータ一覧</h2>
<h3 id="base-parameters">Base Parameters</h3>
<table>
<thead>
<tr>
<th style="text-align:left">name</th>
<th style="text-align:left">example</th>
<th style="text-align:left">memo</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">drive_dir</td>
<td style="text-align:left">/content/drive/MyDrive</td>
<td style="text-align:left">Google Driveのディレクトリパス</td>
</tr>
<tr>
<td style="text-align:left">data_dir</td>
<td style="text-align:left">/content/drive/MyDrive/SRWS-PSG</td>
<td style="text-align:left">train_data, test_data, sample_submissionの格納パス</td>
</tr>
<tr>
<td style="text-align:left">save_dir</td>
<td style="text-align:left">/content/drive/MyDrive/experiments/2021-09-21_235528</td>
<td style="text-align:left">実験結果を格納するディレクトリ</td>
</tr>
<tr>
<td style="text-align:left">model_dir</td>
<td style="text-align:left">/content/drive/MyDrive/experiments/2021-09-21_235528/models</td>
<td style="text-align:left">モデルの保存・読み込みを行うディレクトリ</td>
</tr>
<tr>
<td style="text-align:left">cache_dir</td>
<td style="text-align:left">/content/drive/MyDrive/cache/huggingface/transformers/</td>
<td style="text-align:left">Huggingface Transformers用のキャッシュ</td>
</tr>
<tr>
<td style="text-align:left">model_name</td>
<td style="text-align:left">sultan/BioM-ELECTRA-Base-Discriminator</td>
<td style="text-align:left">Huggingface Transformersで使用可能なモデル名</td>
</tr>
<tr>
<td style="text-align:left">from_pt</td>
<td style="text-align:left">True</td>
<td style="text-align:left">事前学習モデルとしてpytorchのモデルを使用するか否か</td>
</tr>
<tr>
<td style="text-align:left">max_length</td>
<td style="text-align:left">512</td>
<td style="text-align:left">最大トークン数</td>
</tr>
<tr>
<td style="text-align:left">n_splits</td>
<td style="text-align:left">5</td>
<td style="text-align:left">Cross Validationを行う場合の分割数</td>
</tr>
<tr>
<td style="text-align:left">dropout_rate</td>
<td style="text-align:left">0.1</td>
<td style="text-align:left">モデルの最終層のdropout rate</td>
</tr>
<tr>
<td style="text-align:left">epochs</td>
<td style="text-align:left">48</td>
<td style="text-align:left">エポック数</td>
</tr>
<tr>
<td style="text-align:left">steps_per_epoch</td>
<td style="text-align:left">30</td>
<td style="text-align:left">1エポックあたり何ステップとするか</td>
</tr>
<tr>
<td style="text-align:left">train_batch_size</td>
<td style="text-align:left">64</td>
<td style="text-align:left">学習時のバッチサイズ</td>
</tr>
<tr>
<td style="text-align:left">valid_batch_size</td>
<td style="text-align:left">64</td>
<td style="text-align:left">評価時のバッチサイズ</td>
</tr>
<tr>
<td style="text-align:left">test_batch_size</td>
<td style="text-align:left">64</td>
<td style="text-align:left">推論時のバッチサイズ</td>
</tr>
<tr>
<td style="text-align:left">seed</td>
<td style="text-align:left">2021</td>
<td style="text-align:left">ランダムシード</td>
</tr>
<tr>
<td style="text-align:left">target_col</td>
<td style="text-align:left">judgement</td>
<td style="text-align:left">正解ラベルの列名</td>
</tr>
<tr>
<td style="text-align:left">feature_cols</td>
<td style="text-align:left">['title', 'abstract']</td>
<td style="text-align:left">テキストの列名</td>
</tr>
<tr>
<td style="text-align:left">mode</td>
<td style="text-align:left">train</td>
<td style="text-align:left">動作モード、train, evaluate, predict, ensemble から選択</td>
</tr>
<tr>
<td style="text-align:left">folds</td>
<td style="text-align:left">[0, 1, 2, 3, 4]</td>
<td style="text-align:left">Cross Validationのどのfoldを実行するか</td>
</tr>
</tbody>
</table>
<h3 id="optimizer">Optimizer</h3>
<table>
<thead>
<tr>
<th style="text-align:left">name</th>
<th style="text-align:left">example</th>
<th style="text-align:left">memo</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">learning_rate</td>
<td style="text-align:left">0.0001</td>
<td style="text-align:left">学習率</td>
</tr>
<tr>
<td style="text-align:left">weight_decay</td>
<td style="text-align:left">1e-05</td>
<td style="text-align:left"></td>
</tr>
<tr>
<td style="text-align:left">epsilon</td>
<td style="text-align:left">1e-14</td>
<td style="text-align:left"></td>
</tr>
<tr>
<td style="text-align:left">print_change_log</td>
<td style="text-align:left">0</td>
<td style="text-align:left">起動時にパッケージの更新ログを表示するか否か</td>
</tr>
</tbody>
</table>
<h3 id="checkpoint">Checkpoint</h3>
<table>
<thead>
<tr>
<th style="text-align:left">name</th>
<th style="text-align:left">example</th>
<th style="text-align:left">memo</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">monitor</td>
<td style="text-align:left">fbeta_score</td>
<td style="text-align:left">どの評価指標をbest model選択の基準とするか。fbeta_score, aucを選択可能</td>
</tr>
<tr>
<td style="text-align:left">mode</td>
<td style="text-align:left">max</td>
<td style="text-align:left">評価指標を最大にするか最小にするか。min or max</td>
</tr>
<tr>
<td style="text-align:left">default_score</td>
<td style="text-align:left">0.85</td>
<td style="text-align:left">最初のモデル保存のための基準スコア</td>
</tr>
<tr>
<td style="text-align:left">n_best</td>
<td style="text-align:left">3</td>
<td style="text-align:left">bestいくつまでモデルを保持するか</td>
</tr>
</tbody>
</table>
<h3 id="ensemble">ensemble</h3>
<table>
<thead>
<tr>
<th style="text-align:left">name</th>
<th style="text-align:left">example</th>
<th style="text-align:left">memo</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">date</td>
<td style="text-align:left">['2021-09-08_000518', '2021-09-11_043111']</td>
<td style="text-align:left">どの日付のモデルをアンサンブルに使用するか</td>
</tr>
<tr>
<td style="text-align:left">thresholds</td>
<td style="text-align:left">[0.09913, 0.12033]</td>
<td style="text-align:left">日付のモデルに対応した閾値</td>
</tr>
</tbody>
</table>

</body>
</html>
