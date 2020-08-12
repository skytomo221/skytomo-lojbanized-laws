# skytomo式ロジバン化

skytomo式ロジバン化（skaitomon zei jboga'i tadji）では一定の方法で非ロジバンの単語をロジバン化することができます。
このルールに従って大量にロジバン化することができます。
また、これは jbovlaste や Wikipedia における検索などで役に立ちます。

## 大まかな流れ

1. すでに独自の cmevla が割り振られている場合はそれを優先します。
2. 言語ごとに簡易的なルールがある場合はそちらを優先します。
3. IPAからロジバンの音素配列を作ります。
4. ロジバンの音素配列から、cmevlaまたはfu'ivlaを作ります。  
5. 語末を子音にしたいときは s を語末に追加します。
6. 語末を母音にしたいときは i を語末に追加します。

1 の例として、guskant, kocon, skaitomon などがあります。

## IPA からロジバンの音素配列を作る

以下の方法にしたがってIPAをロジバンの音素配列に変換します。

1. 下にある表にしたがって音素配列に変換します。ただし、以下の例外があります。
    1. c + 母音であれば、「kii + 母音」と変換します。
    2. ɟ + 母音であれば、「gii + 母音」と変換します。
    3. ɲ + 母音であれば、「nii + 母音」と変換します。
    4. ŋ + 子音であれば、「n」と変換します。
    5. ç + 母音であれば、「xii + 母音」と変換します。
    6. 間に y を入れることによって子音の禁則配列を回避します。
    7. 間に ' を入れることによって母音の禁則配列を回避します。

<table>
	<tbody>
		<tr>
			<td align="center"></td>
			<td  align="center" colspan="2"><b>唇音</b></td>
			<td  align="center" colspan="4"><b>舌頂音</b></td>
			<td  align="center" colspan="3"><b>舌背音</b></td>
			<td  align="center" colspan="3"><b>咽喉音</b></td>
		</tr>
		<tr>
			<td align="center"></td>
			<td align="center"><b>両唇音</b></td>
			<td align="center"><b>唇歯音</b></td>
			<td align="center"><b>歯音</b></td>
			<td align="center"><b>歯茎音</b></td>
			<td align="center"><b>後部歯茎音</b></td>
			<td align="center"><b>そり舌音</b></td>
			<td align="center"><b>硬口蓋音</b></td>
			<td align="center"><b>軟口蓋音</b></td>
			<td align="center"><b>口蓋垂音</b></td>
			<td align="center"><b>咽頭音</b></td>
			<td align="center"><b>喉頭蓋音</b></td>
			<td align="center"><b>声門音</b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">破裂音</td>
			<td align="center">p b</td>
			<td align="center"></td>
			<td  align="center" colspan="3">t d</td>
			<td align="center">ʈ ɖ</td>
			<td align="center">c ɟ</td>
			<td align="center">k ɡ</td>
			<td align="center">q ɢ</td>
			<td align="center"></td>
			<td align="center">ʡ</td>
			<td align="center">ʔ</td>
		</tr>
		<tr>
			<td align="center"><b>p b</b></td>
			<td align="center"><b></b></td>
			<td  align="center" colspan="4"><b>t d</b></td>
			<td align="center"><b>ki gi</b></td>
			<td align="center" colspan="2"><b>k g</b></td>
			<td align="center">-</td>
			<td align="center">-</td>
			<td align="center">-</td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">鼻音</td>
			<td align="center">m</td>
			<td align="center">ɱ</td>
			<td  align="center" colspan="3">n</td>
			<td align="center">ɳ</td>
			<td align="center">ɲ</td>
			<td align="center">ŋ</td>
			<td align="center">ɴ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center" colspan="2"><b>m</b></td>
			<td align="center" colspan="4"><b>n</b></td>
			<td align="center"><b>ni</b></td>
			<td align="center"><b>ng</b></td>
			<td align="center"><b>n</b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">ふるえ音</td>
			<td align="center">ʙ</td>
			<td align="center" colspan="3">r</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center">ʀ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center"><b>b</b></td>
			<td align="center" colspan="3"><b>r</b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b>r</b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">はじき音</td>
			<td align="center"></td>
			<td align="center">ⱱ</td>
			<td align="center" colspan="3">ɾ</td>
			<td align="center">ɽ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center"><b></b></td>
			<td align="center"><b>v</b></td>
			<td align="center" colspan="4"><b>r</b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">摩擦音</td>
			<td align="center">ɸ β</td>
			<td align="center">f v</td>
			<td align="center">θ ð</td>
			<td align="center">s z</td>
			<td align="center">ʃ ʒ</td>
			<td align="center">ʂ ʐ</td>
			<td align="center">ç ʝ</td>
			<td align="center">x ɣ</td>
			<td align="center">χ ʁ</td>
			<td align="center">ħ ʕ</td>
			<td align="center">ʜ ʢ</td>
			<td align="center">h ɦ</td>
		</tr>
		<tr>
			<td align="center" colspan="2"><b>f v</b></td>
			<td align="center" colspan="2"><b>s z</b></td>
			<td align="center" colspan="2"><b>c j</b></td>
			<td align="center"><b>xi i</b></td>
			<td align="center"><b>x g</b></td>
			<td align="center"><b>x r</b></td>
			<td align="center" colspan="2"><b>x u</b></td>
			<td align="center"><b>x x</b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">接近音</td>
			<td align="center"></td>
			<td align="center">ʋ</td>
			<td align="center" colspan="3">ɹ</td>
			<td align="center">ɻ</td>
			<td align="center">j</td>
			<td align="center">ɰ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center"><b></b></td>
			<td align="center"><b>u</b></td>
			<td align="center" colspan="4"><b>r</b></td>
			<td align="center"><b>i</b></td>
			<td align="center">未定</td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">摩擦音</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center" colspan="3">ɬ ɮ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center" colspan="3">未定</td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
		<tr>
			<td  align="center" rowspan="2">接近音</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center" colspan="3">l</td>
			<td align="center">ɭ</td>
			<td align="center">ʎ</td>
			<td align="center">ʟ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center" colspan="4"><b>l</b></td>
			<td align="center">未定</td>
			<td align="center">未定</td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
        <tr>
			<td  align="center" rowspan="2">はじき音</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center" colspan="3">ɺ</td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
			<td align="center"></td>
		</tr>
		<tr>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center" colspan="3"><b>r</b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
			<td align="center"><b></b></td>
		</tr>
	</tbody>
</table>

|  IPA  |   音素配列   |
| :---: | :----------: |
|  ɕ ʑ  | **c** **j**  |
|   ɧ   |    **c**     |
|   ɫ   |    **l**     |
|   ɥ   |    **u**     |
|  ʍ w  | **u**  **u** |

|      IPA      | 音素配列 |
| :-----------: | :------: |
| a ɑ ʌ æ ɐ ɶ ä |  **a**   |
|  ɛ e ø ɘ e̞ ø̞  |  **e**   |
|  i y ɨ ɪ ʏ ɪ̈  |  **i**   |
| o ɔ ɵ ɤ ɤ̞ o̞ ɒ |  **o**   |
|  u ɯ ʉ ʊ̈ ɯ̽ ʊ  |  **u**   |
|       ə       |  **y**   |

### IPA からロジバンの音素配列の変換例

- Python → [ˈpaɪθɑːn] → *paisan*
- spaghetti （スパゲッティ） → [spaˈɡetti] → *spageti*
- 東京 → [to̞ːkʲo̞ː] → *tokiio*

## ロジバンの音素配列から cmevla を作る

1. 語末が子音であればそれが cmevla になります。
2. 語末が母音であれば s を語末に追加して cmevla を作ります。

### ロジバンの音素配列から cmevla の変換例

- Albert Einstein → [ˈalbɛʁt ˈʔaɪnʃtaɪn] → *albert ainctain* → **albert ainctain**
- Esperanto → [es.peˈran.to] → *esperantos* → **esperantos**
- キズナアイ → [kʲizɨᵝna̠ a̠i] → *kiiizuna ai* → **kiiizunas ais**
- 李 → [lì] → *li* → **lis**
- 東京 → [to̞ːkʲo̞ː] → *tokiio* → **tokiios**
- Twitter → [ˈtwɪ.tə(ɹ)] → *tuuityr* → **tuuityr**

## ロジバンの音素配列から一型フヒブラを作る

1. {me la'o zoi .ロジバンの音素配列. zoi} とします。

### ロジバンの音素配列から一型フヒブラの変換例

- spaghetti → [spaˈɡetti] → *spageti* → me la'o zoi .*spageti*. zoi

## ロジバンの音素配列から二型フヒブラを作る

1. {me la CMENE} とします。

cmevla の作り方は「ロジバンの音素配列から cmevla を作る」方法とまったく同じです。

### ロジバンの音素配列から二型フヒブラの変換例

- spaghetti → [spaˈɡetti] → *spageti* → me la .spagetis.

## ロジバンの音素配列から三型フヒブラを作る

1. 音素配列の語末が子音であれば i を語末に追加します。
2. 4文字ラフシを以下の表に従って選びます。
3. 4文字ラフシと音素配列の間に必要に応じて r, n, l （優先度順）を挟みます。
4. 語頭が母音であれば先頭の4文字ラフシによって条件が変わります。
   1. 先頭の4文字ラフシの語末が子音になるならば何もしません。
   2. 先頭の4文字ラフシの語末が必ず母音ならば音素配列の語頭に ' を追加します。

### ロジバンの音素配列から三型フヒブラの変換例

- spaghetti → [spaˈɡetti] → *spageti* → cidja + spageti → dja + r + spageti → **djarspageti**
- origami → *origami* → larcu + origami → lar + n + origami → **larnorigami**

※ [「larnorigami」のままでは最初の５字が gimvla となって「larno ri ga mi」等のようにばらける](https://ja.wikibooks.org/wiki/%E3%83%AD%E3%82%B8%E3%83%90%E3%83%B3/%E5%BD%A2%E6%85%8B%E8%AB%96#fu'ivla%20%E7%B3%BB)ので、「larnxorigami」のように、外来語部分が母音で始まる場合はこれを子音で始まるように変えないといけないみたいなのですが、
**だったらどうして「[banjupunu](http://misonikomilojban.blogspot.com/2013/10/iso.html)」は「banju pu nu」に分解されないんですか？**
私にはわかりませんので、今のところは無視します。

## ロジバンの音素配列から四型フヒブラを作る

※正直、四型フヒブラ分からないので、やべーこと書いてるかもしれません。
特に問題がない場合は教えてください。
逆に問題がある場合は教えてください。
お願いします。

1. 音素配列の語末が子音であれば i を語末に追加します。

上から順に試して fu'ivla になれば完成です。

1. 2番目の母音を消す
2. 語頭にsをつける
3. 語頭にzをつける
4. 語頭にdをつける
5. 最初の子音の後ろに r, l, n, rl, lr, rln （優先度順）をつける
6. 2番目の子音の直前に r, l, n, rl, lr, rln （優先度順）を入れる
7. 2番目の子音がない場合は2音節目に rli, lri, rlni （優先度順）を追加する

### ロジバンの音素配列から四型フヒブラの変換例

- igloo（イーグル） → *iglu* → **iglu** （存在が四型フヒブラなのでそのまま完成）
- ぽんぽんぺいん → *pompompein* → **pompompeini** （存在が四型フヒブラなのでそのまま完成）
- スパゲッティ → *spageti* → **spageti** （存在が四型フヒブラなのでそのまま完成）
- アニメ → *anime* → **anme** （1で完成）
- 浦島効果 → *uracimako'uka* → **urcimako'uka** （1で完成）
- 腹切り → *xarakiri* → **xarkiri** （1で完成）
- 唐揚げ → *kara'age* → **skara'age** （2で完成）
- 牛丼 → *giiudon* → **zgiiudoni** （3で完成）
- じゃがりこ → *jagariko* -> **djagariko** （4で完成）
- ハヤシライス → *xaiaciraisu* → **xraiaciraisu** （5で完成）
- 寿司 → *suci* → **srluci** （5で完成）
- 鬼 → *oni* → **onri** （5で完成）
- 忍者 → *ninja* → **nirnja** （6で完成）
- 蘇 → *so* → **sorlni** （7で完成）
- 大鬼 → *o'o'oni* → **orli'o'oni** （7で完成）

※日本語多いので日本語以外の例があればください。
