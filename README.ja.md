# skytomo式cmevla

skytomo式cmevla（skaitomon zei cmevla ciste）は一定の方法で単語をcmevlaにするシステムです。
これは jbovlaste や Wikipedia における検索などで役に立ちます。

## 大前提

1. 基本的にIPAを基準に変換します。
2. 言語ごとに簡易的なルールがある場合はそちらを優先します。
3. 語末を子音にしたいときは s を語末に追加します。
4. 語末を母音にしたいときは i を語末に追加します。

## IPA から cmevla を作る

1. 対象のものに対してすでに独自の cmevla が割り振られている場合はそれを優先します。
   - 【例】 guskant
   - 【例】 kocon
   - 【例】 skaitomon
2. 以下の方法にしたがってIPAをロジバンの音素配列に変換します。
   1. ロジバンに存在する発音はそのまま音素配列になります。
   2. 下にある表にしたがって音素配列に変換します。ただし、以下の例外があります。
      1. ɲ + 母音であれば、「nii + 母音」と変換します。
      2. ŋ + 子音であれば、「n」と変換します。
      3. ç + 母音であれば、「xii + 母音」と変換します。
      4. 間に y を入れることによって子音の禁則配列を回避します。
      5. 間に ' を入れることによって母音の禁則配列を回避します。
   - 【例】 Albert Einstein [ˈalbɛʁt ˈʔaɪnʃtaɪn] → *albert ainctain* → **albert ainctain**
3. 以下の方法にしたがってロジバンの音素配列をcmevlaに変換します。
   1. 語末が子音であればそれが cmevla になります。
         - 【例】 Albert Einstein [ˈalbɛʁt ˈʔaɪnʃtaɪn] → *albert ainctain* → **albert ainctain**
   2. 語末が母音であれば語末を子音にしたいときは s を語末に追加して cmevla を作ります。
         - 【例】 キズナアイ [kʲizɨᵝna̠ a̠i] → *kiiizuna ai* → **kiiizunas ais**
         - 【例】 李 [lì] → *li* → **lis**
         - 【例】 東京 [to̞ːkʲo̞ː] → *tokiio* → **tokiios**
         - 【例】 Esperanto [es.peˈran.to] → *esperantos* → **esperantos**

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
			<td  align="center" colspan="3"><b>t d</b></td>
			<td align="center"><b>t d</b></td>
			<td align="center"><b>ki gi</b></td>
			<td align="center"><b>k g</b></td>
			<td align="center"><b>k g</b></td>
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

|      IPA      | 音素配列 |
| :-----------: | :------: |
| a ɑ ʌ æ ɐ ɶ ä |  **a**   |
|  ɛ e ø ɘ e̞ ø̞  |  **e**   |
|  i y ɨ ɪ ʏ ɪ̈  |  **i**   |
| o ɔ ɵ ɤ ɤ̞ o̞ ɒ |  **o**   |
|  u ɯ ʉ ʊ̈ ɯ̽ ʊ  |  **u**   |
|       ə       |  **y**   |

## 例

- [日本の都道府県の例](example/Prefectures%20of%20Japan.tsv)
