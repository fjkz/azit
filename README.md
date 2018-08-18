AZIT
====

コンセプト
----------

日本語入力を効率化するためのローマ字入力法です。

[AZIK](http://hp.vector.co.jp/authors/VA002116/azik/azikinfo.htm)を参考にしています。作者がAZIKの設定ファイルを作る際に間違ってAZITとつけてしまったのでそれを名前にしました。

以下の方針で設計しています。

* 使用頻度の高い二重母音・撥音は新たな母音としてキーを当てる。
* 使用頻度の高い拗音には新たな子音としてキーを当てる。
* 使用頻度の低い音は捨てて、使用頻度の高い音を書きやすくする。
* 英語の綴りに近い書き方ができるようにする。
* 分かりきった母音は省略できるようにする。

設定方法
--------

Google日本語入力（Mozc）用の設定ファイル

- mozc\_azit.txt

を用意しています。

設定方法は以下の通りです。

1. Google日本語入力の「プロパティ」を開く。
2. 「一般」タブ > ローマ字テーブル「編集」のボタンを押す。
3. 「編集」 ボタン > 「インポート」を選択する。
4. 「現在のローマ字テーブルを上書きしますか?」と表示されるので「OK」を押す。
5. ダウンロードしたGoogle日本語入力用の設定ファイルを選択する。

入力方法
--------

### 拗音

従来、拗音には「\*y\*」か「\*h\*」を用いていましたが、AZITでは「\*j\*」を使用します。例えば、

> gjarndju        → ぎゃらんどぅ

> qari:pamjupamju → きゃりーぱみゅぱみゅ

となります。英語に「\*y\*」は存在しないし、英語以外の言語は「j」は「ヤ」か「ハ」の音なので、違和感は少ないかと思います。ただ、他の簡便なキーで代替可能なので、慣れてくると「\*j\*」はほとんど使用しなくなると思います。また、後述の母音拡張は「\*j\*」に対しては効果が低いので用意していません。

使用頻度の多い「しゃ」行・「ちゃ」行・「りゃ」行・「きゃ」行はそれぞれ子音に「x」・「c」・「l」・「q」の１字を使用することもできます。例えば、

> xach → しゃちょう

> qwlh → きゅうりょう

となります。

「ぢ」は「でぃ」と比べて使用頻度が少ないので、「di」には「でぃ」を当てています。「ぢ」には「dji」を使用してください。

> dizuni: → でぃずにー

> hanadji → はなぢ

となります。「ち」は「ci」でも書けますが、使用頻度が多くローマ字入力に慣れた指が覚えていることから「ti」を残しています。「てぃ」と書くには「tji」としてください。

> nltjivu → ねいてぃぶ

「どぅ」は「dw」を、「でゅ」は「dju」を使います。

> dwkatji → どぅかてぃ

> djupb   → でゅぽん

「hu」は「フ」の音でなく、「ふ」と書く場合は通常「fu」を使用するので、「hu」には「ひゅ」を当てています。
ほとんどの場合、「ヒュー」と伸ばすので「hw」には「ひゅー」を当てています。

> huuga → ひゅうが

> hwmn  → ひゅーまん

同様に「vw」も「びゅー」、「pw」も「ぴゅー」となります。

> revw → れびゅー
> kompwtar; → こんぴゅーたー

また、「\*v」で「\*ょう」を書くこともできます。例えば、

> bvjh → びょうじょう

> gvxh → ぎょうしょう

となります。

「ぁ」「ゃ」「ヵ」等の拗音に添える小さい字を入力する際は「@\*」を使用します。

> @a  → ぁ

> @ya → ゃ

> @ka → ヵ

これらの字を文章を書く際に直接入力することは推奨しません。書き方が複雑な言葉は、IMEのユーザー辞書に登録するべきと考えています。

### 長音

ハイフン「-」・コロン「:」で長音記号「ー」を書きます。

> \- → ー

> :  → ー

「：」の入力には「v:」・「@:」を使用します。

> v: → ：

> @: → ：

また、「r;」も「ー」になります。

> bar; → ばー

### 促音

「;」または「vv」で「っ」を書けます。

> ha; → はっ

> vvavva → っあっあ

「;」の入力には「v;」・「@;」を使用します。

> v; → ；

> @; → ；

よく使う促音については従来どおり2回子音を重ねることで促音にできます。

> sikkari → しっかり

> sippf   → しっぱい

> sossd   → そっせん

> jitty   → じったい

> baffa   → ばっふぁ

ただし、「dd」・「gg」は促音になりません。この点はぎこちないです。

> ddcw → でんちゅう

> ggkh → ぎんこう

カタカナ語に頻出する「っく」・「っぐ」・「っと」・「っど」・「っくす」は子音１字＋セミコロンで書けます。

> pik;   → ぴっく

> panic; → ぱにっく

> big;   → びっぐ

> met;   → めっと

> red;   → れっど

> mix;   → みっくす

### 撥音

「ん」は従来どおりに「nn」でかけます。「n;」も使用できます。

> nn → ん

> n; → ん

ただし、「n」+子音では「ん」にはなりません。

「ぱん」・「ぴん」・「くん」・「べん」・「ぼん」等の２文字目に「ん」がくるものについては、例えば

> pann → ぱん

と書くこともできますが、「an;」の代わりに「n」と打つことで、

> pn → ぱん

と書けば良くなります。以下の５つの撥音を省略することができます。

| 従来 | 代替 | 由来            |
|------|------|-----------------|
| ann  | n    | pan（パン）のn  |
| inn  | g    | ping（ピン）のg |
| unn  | m    | um（ウン）のm   |
| enn  | d    | bend（ベン）のd |
| onn  | b    | bomb（ボン）のb |

例えば、

> sgbm → しんぶん

> gbgd → ごんげん

> dnrn → だんらん

となります。

「なん」は例外で、

> nannpa → なんぱ

### 二重母音

母音が連続するものです。例えば

> bai → ばい

の代わりに、

> by → ばい

と書けます。以下の４つの二重母音を省略できます。

| 従来 | 代替 | 由来                              |
|------|------|-----------------------------------|
| ai   | y, f | by（バイ）のy、knife（ナイフ）のf |
| uu   | w    | new（ニュウ）のw                  |
| ei   | l    | tail（テイル）のl                 |
| ou   | h    | oh（オウ）のh                     |

例えば、

> qhtl → きょうてい

> xhty → しょうたい

> kwsh → くうそう

> nfzf → ないざい

となります。ただし、「nw」は「にゅう」となります。

> nwloku → にゅうりょく

「ai」は頻出し、「y」だけでは打ちづらい場合があるので「f」も当てています。ただし、「ff」は撥音となります。「ふぁい」は「fy」と書いて下さい。

### 無音子音

「v」を void からとって無音の子音としています。

> vnsg → あんしん

> vhvd → おうえん

ただし、「vw」は「びゅー」となります。「ヴぁ」行には、「vj\*」を当てています。

### 句読点前の母音

子音のあとに句読点を打つと、母音を挿入します。例えば、

> sr.    → する。

> sit.   → した。

> shd.   → そうだ。

> sosit, → そして、

になります。動詞の活用や助詞を考慮して、最もありそうな母音を入れています。

### 省略形

よく使う言葉は省略して書くこともできます。

> kto   → こと

> tki   → とき

> rsii  → らしい

> mta   → また

> sks,  → しかし、

> ds.   → です。

> ms.   → ます。

> tsr.  → とする。

> dkir. → できる。

> dz.   → である。

### 英語風入力

一部の英単語は英語の綴りを入力するとカタカナ読みになります。

> fry       → ふらい

> craft     → くらふと

> sick      → しっく

> disc      → でぃすく

> ant       → あんと

> abenomics → あべのみくす

> milk      → みるく

> spark     → すぱーく

> egoist    → えごいすと

> kinect    → きねくと

> next      → ねくすと

子音で終わる単語は「;」をつける必要があります。

> input;   → いんぷっと

> fix;     → ふぃっくす

> dog;     → どっぐ

> nul;     → ぬる

ローマ字表
----------

横列が子音、縦列が母音です。表はすべての変換は網羅していません。

|       |    | v      | k     | s      | t      | n      | h      | m      | y    |
|-------|----|--------|-------|--------|--------|--------|--------|--------|------|
| **a** | あ | あ     | か    | さ     | た     | な     | は     | ま     | や   |
| **i** | い | い     | き    | し     | ち　   | に     | ひ     | み     |      |
| **u** | う | う     | く    | す     | つ     | ぬ     | ふ     | む     | ゆ   |
| **e** | え | え     | け    | せ     | て     | ね     | へ     | め     |      |
| **o** | お | お     | こ    | そ     | と     | の     | ほ     | も     | よ   |
| **n** |    | あん   | かん  | さん   | たん   | ん     | はん   | まん   | やん |
| **g** |    | いん   | きん  | しん   | ちん　 | にん   | ひん   | みん   |      |
| **m** |    | うん   | くん  | すん   | つん   | ぬん   | ふん   | むん   | ゆん |
| **d** |    | えん   | けん  | せん   | てん   | ねん   | へん   | めん   |      |
| **b** |    | おん   | こん  | そん   | とん   | のん   | ほん   | もん   | よん |
| **y** |    | あい   | かい  | さい   | たい   | ない   | はい   | まい   | やい |
| **f** |    | あい   | かい  | さい   | たい   | ない   | はい   | まい   | やい |
| **w** |    | びゅー | くう  | すう   | つう   | にゅう | ひゅー | むう   | ゆう |
| **l** |    | えい   | けい  | せい   | てい   | ねい   | へい   | めい   |      |
| **h** |    | おう   | こう  | そう   | とう   | のう   | ほう   | もう   | よう |
| **v** |    | っ     | きょう| しょう |        | にょう | ひょう | みょう | よう |
| **.** | 。 |        | く。  | す。   | た。   | ん。   |        | む。   |      |
| **,** | 、 |        | く、  | し、   | て、   | に、   | は、   | み、   |      |
| **;** | っ | ；     | っく  | す     | っと   | ん     | う     | む     | い   |

|       | r      | w      | g      | z    | d      | b      | p      |
|-------|--------|--------|--------|------|--------|--------|--------|
| **a** | ら     | わ     | が     | ざ   | だ     | ば     | ぱ     |
| **i** | り     | うぃ   | ぎ     | じ   | でぃ   | び     | ぴ     |
| **u** | る     | う     | ぐ     | ず   | づ     | ぶ     | ぷ     |
| **e** | れ     | うぇ   | げ     | ぜ   | で     | べ     | ぺ     |
| **o** | ろ     | を     | ご     | ぞ   | ど     | ぼ     | ぽ     |
| **n** | らん   | わん   | がん   | ざん | だん   | ばん   | ぱん   |
| **g** | りん   | うぃん | ぎん   | じん | でぃん | びん   | ぴん   |
| **m** | るん   |        | ぐん   | ずん | づん   | ぶん   | ぷん   |
| **d** | れん   |        | げん   | ぜん | でん   | べん   | ぺん   |
| **b** | ろん   | うぉん | ごん   | ぞん | どん   | ぼん   | ぽん   |
| **y** | らい   | わい   | がい   | ざい | だい   | ばい   | ぱい   |
| **f** | らい   | わい   | がい　 | ざい | だい   | ばい 　| ぱい   |
| **w** | るう   |        | ぐう   | ずう | どぅ   | ぶう   | ぴゅー |
| **l** | れい   |        | げい   | ぜい | でい   | べい   | ぺい   |
| **h** | ろう   | うぉー | ごう   | ぞう | どう   | ぼう   | ぽう   |
| **v** | りょう |        | ぎょう |      |        | びょう | ぴょう |
| **.** | る。   |        | ぐ。   | ず。 | だ。   | ぶ。   |        |
| **,** | り、   |        | が、   | ず、 | で、   | ば、   |        |
| **;** | ー     | ー     | っぐ   | ず   | っど   | ぶ　   | っぷ   |

|       | f      | q      | x      | c      | l      | j      |
|-------|--------|--------|--------|--------|--------|--------|
| **a** | ふぁ   | きゃ   | しゃ   | ちゃ   | りゃ   | じゃ   |
| **i** | ふぃ   | くぃ   | し     | ち     | り     | じ     |
| **u** | ふ     | きゅ   | しゅ   | ちゅ   | りゅ   | じゅ   |
| **e** | ふぇ   | くぇ   | しぇ   | ちぇ   | れ     | じぇ   |
| **o** | ふぉ   | きょ   | しょ   | ちょ   | りょ   | じょ   |
| **n** | ふぁん | きゃん | しゃん | ちゃん | りゃん | じゃん |
| **g** | ふぃん | くぃん | しん   | ちん   | りん   | じん   |
| **m** | ふん   | きゅん | しゅん | ちゅん | りゅん | じゅん |
| **d** | ふぇん | くぇん | しぇん | ちぇん | れん   | じぇん |
| **b** | ふぉん | きょん | しゃん | ちょん | りょん | じょん |
| **y** | ふぁい | きゃい | しゃい | ちゃい | りゃい | じゃい |
| **f** | ふぁい | きゃい | しゃい | ちゃい | りゃい | じゃい |
| **w** | ふう   | きゅう | しゅう | ちゅう | りゅう | じゅう |
| **l** | ふぇい | くぇい | しぇい | ちぇい | れい   | じぇい |
| **h** | ふぉー | きょう | しょう | ちょう | りょう | じょう |
| **v** | ふゅー | きょう | しょう | ちょう | りょう | じょう |
| **.** |        |        |        |        |        |        |
| **,** |        |        |        |        |        |        |
| **;** | ふ     | っく   | っくす | っく   | る     |        |

|       | tj   | nj   | hj   | mj   | wj   | fj   | gj   | dj   | bj   | vj   | pj   |
|-------|------|------|------|------|------|------|------|------|------|------|------|
| **a** | つぁ | にゃ | ひゃ | みゃ | うぁ | ふゃ | ぎゃ | ぢゃ | びゃ | ヴぁ | ぴゃ |
| **i** | てぃ | にぃ | ひぃ | みぃ | ゐ   | ふぃ | ぎぃ | ぢ   | びぃ | ヴぃ | ぴゃ |
| **u** | とぅ | にゅ | ひゅ | みゅ | うぅ | ふゅ | ぎゅ | でゅ | びゅ | ヴぅ | ぴゃ |
| **e** | つぇ | にぇ | ひぇ | みぇ | ゑ   | ふぇ | ぎぇ | ぢぇ | びぇ | ヴぇ | ぴぇ |
| **o** | つぉ | にょ | ひょ | みょ | うぉ | ふょ | ぎょ | ぢょ | びょ | ヴぉ | ぴょ |

|        | @  | @k | @t | @y |
|--------|----|----|----|----|
| **a**  | ぁ | ヵ |    | ゃ |
| **i**  | ぃ |    |    |    |
| **u**  | ぅ |    | っ | ゅ |
| **e**  | ぇ | ヶ |    |    |
| **o**  | ぉ |    |    | ょ |

おまけ
------

通常、IMEのon/offには「全角／半角」キーを用います。
しかし、日本語と英単語が混在する文章を書くときには、このキーは遠いので不便を感じます。
また、「vim」エディタを使用すると、「Esc」キーと誤って「半角／全角」キーを押してしまって混乱してしまうことがあります。
そこで、IMEのon/offには「変換」キーを使うことを提案しています。

- `mozc_keymap.txt`

は、Google日本語入力（Mozc）用キー設定ファイルです。

なお、通常の設定でもカタカナへの変換は「F7」キーだけでなく「無変換」キーでも行うことができるので、使用すると便利だと思います。

