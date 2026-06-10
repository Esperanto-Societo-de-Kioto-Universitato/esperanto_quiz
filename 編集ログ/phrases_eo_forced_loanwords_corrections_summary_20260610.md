# エスペラント例文 強引な外来語・カルク修正一覧

作成日: 2026-06-10

対象ファイル: `phrases_eo_en_ja_zh_ko_ru_fulfilled_260505.csv`

## 概要

`minibaro` 級の強引な外来語化や、英語・ロシア語の連語をそのまま移したような表現を点検し、エスペラント学習教材として明確に直した方がよい箇所だけを修正した。

最終的なCSV差分は **69行**。音声差し替え操作は **71件** だが、これは PID 2271 と PID 3248 を途中でさらに再調整したためで、最終CSV上の変更行数は69行である。

## 判断方針

- 表現が正しい範囲内なら、教材としての多様性を尊重して維持する。
- PIV / ReVo / 既存コーパス内の用法を見て、明確な意味ズレ・非文法・強い内部不整合があるものだけを修正する。
- 料理名・現代的職名・口語として成立する表現は、過度に純化しない。
- 修正後は RHVoice `spomenka` で音声を再生成し、root音声とスマホ用音声を同期する。

## 件数

| 区分 | 内容 | 件数 |
|---|---:|---:|
| 最終CSV変更行 | 現在CSVとHEADの比較で確認した変更行 | 69 |
| 音声生成操作 | 第1・第2・第3・最終検品の合計 | 71 |
| root例文音声 | `Esperanto例文5000文_収録音声/` のWAV | 5000 |
| スマホ例文音声 | `mobile_app/sentence-audio/` のWAV | 5000 |
| Drive fallback | 必要な5000件はアップロード後に全一致 | matched 5000 / missing 0 |
| Drive上の旧重複 | 手作業削除後に解消 | 0 |

## 最終修正一覧

| PID | 修正前 | 修正後 | 主な理由 |
|---:|---|---|---|
| 190 | `Delonge ni ne vidiĝis` | `Delonge ni ne intervidiĝis` | 「互いに会う」の意味を明確化 |
| 374 | `Ĉu mi povus havi vian atenton?` | `Vian atenton, mi petas!` | 英語的な `have attention` を回避 |
| 753 | `Ĉu mi povas havi vian nomon kaj adreson?` | `Ĉu vi bonvolus diri al mi vian nomon kaj adreson?` | 名前・住所を「持つ」許可ではなく、伝えてもらう表現へ |
| 769 | `Ĉio estos bone kun vi` | `Vi fartos bone` | 露語・英語的な構文を自然化 |
| 826 | `Ni penos fari lian fotoroboton` | `Ni penos fari lian portreton laŭ priskribo` | `fotoroboto` を避け、説明に基づく人物像を透明化 |
| 998 | `Li estas en rilato` | `Li havas amrilaton` | 恋愛関係を明示 |
| 1201 | `Ni manĝu ekstere hodiaŭ vespere` | `Ni manĝu eksterhejme hodiaŭ vespere` | 外食の意味で、屋外食との混同を避ける |
| 1208 | `Ĉu vi renkontiĝas kun iu?` | `Ĉu vi havas amrilaton kun iu?` | 「交際している」の意味を明確化 |
| 1301 | `Fraŭlino Wane baldaŭ fariĝos sinjorino Jones` | `Fraŭlino Wayne baldaŭ fariĝos sinjorino Jones` | 固有名 Wayne に修正。英語列も同時修正 |
| 1559 | `Per kio vi gajnas vian vivon?` | `Per kio vi vivtenas vin?` | `gajni sian vivon` は避け、生活を支える表現へ |
| 1703 | `Ĉu vi estas komputile klera?` | `Ĉu vi estas lerta pri komputiloj?` | `computer literate` 直訳感を回避 |
| 1734 | `Ĉu mi ricevos vojaĝkostojn?` | `Ĉu oni repagos al mi la vojaĝkostojn?` | 受け取る対象を「費用」ではなく返金として明確化 |
| 1764 | `Ŝi estos bonega aldono al via programo` | `Ŝi estos tre valora por via programo` | 人を `aldono` とする直訳感を回避 |
| 1841 | `Daŭrigu rekte antaŭen ĉirkaŭ unu kilometron` | `Iru plu rekte antaŭen ĉirkaŭ unu kilometron` | 無目的語 `Daŭrigu` を道案内として自然化 |
| 1853 | `Daŭrigu preter la fajrobrigadejo` | `Iru plu preter la fajrobrigadejo` | 同上 |
| 1854 | `Daŭrigu ankoraŭ ducent metrojn` | `Iru plu ankoraŭ ducent metrojn` | 同上 |
| 1855 | `Daŭrigu ankoraŭ duonkilometron` | `Iru plu ankoraŭ duonkilometron` | 同上 |
| 1856 | `Daŭrigu rekte preter kelkaj semaforoj` | `Iru plu rekte preter kelkaj semaforoj` | 同上 |
| 1921 | `Mi ŝatus grandigi ĉi tiujn fotografiojn` | `Mi ŝatus grandigi ĉi tiujn fotojn` | 可算の写真として既存語 `fotoj` に統一 |
| 1968 | `Sur ĉi tiu aviadilo ne plu estas lokoj` | `En ĉi tiu aviadilo ne plu estas lokoj` | 機内は `en aviadilo` が自然 |
| 1987 | `Ĉu estas liberaj lokoj sur ĉi tiu flugo?` | `Ĉu estas liberaj lokoj por ĉi tiu flugo?` | 便に対する空席として `por` へ |
| 2158 | `Ĉu sur la aviadilo estas stevardino, kiu parolas la hebrean?` | `Ĉu en la aviadilo estas stevardino, kiu parolas la hebrean?` | 機内は `en aviadilo` |
| 2271 | `Kie estas la parkometro?` | `Kie estas la pagmaŝino por parkumado?` | `parkometro` を避けつつ、支払い機の焦点を保持 |
| 2290 | `Vi pasos superbazaron maldekstre` | `Vi preterpasos superbazaron maldekstre` | 「通り過ぎる」は `preterpasi` |
| 2464 | `Mi ŝatus aldoni 10 funtojn al ĝi` | `Mi ŝatus aldoni 10 pundojn al ĝi` | 通貨ポンドは `pundoj` に統一 |
| 2620 | `Ĉu en la ĉambro estas televido?` | `Ĉu en la ĉambro estas televidilo?` | 機器は `televidilo` |
| 2640 | `Mi ŝatus fari rezervon` | `Mi ŝatus rezervi` | `make a reservation` 直訳を避ける |
| 2684 | `Mi faris rezervon` | `Mi rezervis` | 同上 |
| 2704 | `Rezervoj estis faritaj por mi kaj mia familio` | `Ĉambroj estas rezervitaj por mi kaj mia familio` | 予約対象を明確化 |
| 2870 | `Mi bezonas detergenton` | `Mi bezonas deterganton` | PIV派生形 `deterganto` に修正 |
| 2885 | `Mi bezonas rulon da adherema filmo` | `Mi bezonas rulon da adhera plastfolio` | `cling film` 直訳感を抑える |
| 2918 | `Ĉu vi povus fari rezervon por mi?` | `Ĉu vi povus rezervi tablon por mi?` | レストラン文脈の予約対象を明確化 |
| 2923 | `Ĉu vi povas rekomendi picerion?` | `Ĉu vi povas rekomendi picejon?` | PIV掲載の `picejo` に修正 |
| 2925 | `Kien vi kutime iras, kiam vi manĝas ekstere?` | `Kien vi kutime iras, kiam vi manĝas eksterhejme?` | 外食の意味を明確化 |
| 3013 | `Kion vi ŝatus havi?` | `Kion vi ŝatus mendi?` | 注文文脈で `havi` を避ける |
| 3053 | `Ĉu la manĝaĵo venas kun legomoj?` | `Ĉu la manĝaĵo estas servata kun legomoj?` | 英語 `come with` 直訳を回避 |
| 3192 | `La sekvan rondon mi pagas` | `La sekvajn trinkaĵojn mi pagas` | 酒席の英語 `round` 直訳を回避 |
| 3226 | `Ĉu vi ŝatas fumitan viandon?` | `Ĉu vi ŝatas fumaĵitan viandon?` | 燻製は `fumaĵi` 系 |
| 3229 | `Mi prenos la fumitan truton` | `Mi prenos la fumaĵitan truton` | 同上 |
| 3232 | `Mi ŝatus la grilitan salmon` | `Mi ŝatus la kradrostitan salmon` | 料理のグリルは `kradrostita` |
| 3248 | `Li havos grilitan karpon` | `Li prenos kradrostitan karpon` | `grilita` と飲食の `havi` を同時に修正 |
| 3298 | `Li havos kelkajn tomatojn` | `Li manĝos kelkajn tomatojn` | 食べる意味の `havi` を回避 |
| 3330 | `Li ŝatas kaperojn` | `Li ŝatas kaporojn` | 食用ケッパーは `kaporo` |
| 3334 | `Li havos iom da faboj` | `Li manĝos iom da faboj` | 食べる意味の `havi` を回避 |
| 3347 | `Mi ŝatas cerealojn` | `Mi ŝatas cerealaĵojn` | 朝食用シリアルとして `cerealaĵo` |
| 3526 | `Ĉu estas certifikato por ĝi?` | `Ĉu estas atestilo por ĝi?` | 証明書は既存コーパスの `atestilo` に統一 |
| 3568 | `Ĉu ĝi venas kun instrukcioj?` | `Ĉu instrukcioj estas inkluzivitaj?` | 英語 `come with` 直訳を回避 |
| 3682 | `Mi ŝatus duonduzenon da ovoj` | `Mi ŝatus ses ovojn` | 非PIV寄りの `duonduzeno` を数詞で明確化 |
| 3788 | `Tiam mi iros ien alian` | `Tiam mi iros aliloken` | `ien alian` の非文法性を修正 |
| 3999 | `Kiom kostas lui malsekkostumon por unu tago?` | `Kiom kostas lui plonĝkostumon por unu tago?` | `wetsuit` 直訳を避ける |
| 4014 | `Estis remiso` | `La rezulto estis egala` | 不安定な借用形を透明化 |
| 4171 | `Ĉu vi volas, ke mi ŝaltu la televidon?` | `Ĉu vi volas, ke mi ŝaltu la televidilon?` | 機器は `televidilo` |
| 4284 | `Mi ŝatus fari retiron` | `Mi ŝatus elpreni monon` | 銀行出金の `make a withdrawal` 直訳を回避 |
| 4291 | `Mi bezonas formularon por monretiro` | `Mi bezonas formularon por elpreno de mono` | 出金表現を `elpreni/elpreno de mono` に統一 |
| 4296 | `Ĉu mi povas retiri monon de mia kreditkarto ĉi tie?` | `Ĉu mi povas elpreni monon per mia kreditkarto ĉi tie?` | `retiri monon` の出金語義を避ける |
| 4303 | `Mi ŝatus retiri 100 pundojn, mi petas` | `Mi ŝatus elpreni 100 pundojn, mi petas` | 同上 |
| 4341 | `Necesas deponaĵo je unu-monata lupago` | `Necesas kaŭcio egala al unu-monata lupago` | 敷金は `kaŭcio` |
| 4385 | `Mi ŝatus ilin farbigi` | `Mi ŝatus tinkturigi miajn harojn` | 髪を染める文脈は `tinkturi/tinkturigi` |
| 4387 | `Bonvolu farbi miajn harojn blonde` | `Bonvolu tinkturi miajn harojn blonde` | 同上 |
| 4403 | `Malantaŭe kojne, mi petas` | `Malantaŭe laŭgrade mallongigite, mi petas` | 髪型指示として意味を透明化 |
| 4411 | `Ĉu vi ŝatus ion sur ĝi?` | `Ĉu mi metu ion sur la harojn?` | 指示対象不明の `ĝi` を避ける |
| 4419 | `Mi ŝatus havi traktadon de la vizaĝo` | `Mi ŝatus haŭtflegadon de la vizaĝo` | `treatment` 直訳を避ける |
| 4455 | `Ĉu vi povas ripari la televidon?` | `Ĉu vi povas ripari la televidilon?` | 機器は `televidilo` |
| 4561 | `Mi sentas min kapturna` | `Mi havas kapturnon` | めまいの自然表現へ |
| 4650 | `Vi devus redukti vian trinkadon` | `Vi devus redukti vian alkoholtrinkadon` | 飲酒量を明確化 |
| 4708 | `Li havas grandajn dioptriojn` | `Li bezonas fortajn okulvitrojn` | 光学単位の所有表現を回避 |
| 4802 | `Kiun mobilan reton vi havas?` | `Kiun poŝtelefonan reton vi havas?` | `mobile network` 直訳感を避ける |
| 4871 | `Je kioma horo li estas atendata reveni?` | `Je kioma horo oni atendas, ke li revenos?` | 英語風受動構文を自然化 |
| 4941 | `Bonvolu pezi ĉi tiun pakaĵon` | `Bonvolu pesi ĉi tiun pakaĵon` | 他動詞「量る」は `pesi` |

## 主に維持した候補

以下は、Claude Code 側で候補化されたが、教材として正しい範囲内の多様性・現代語・文化語として維持したもの。

- `toasto`, `feni`, `smuzio`, `regato`, `vendmanaĝero`
- `naĉoj`, `kalzoneo`, `servi la pilkon`, `viva muziko`
- `belaruso`, `informatiko`, `konstruktiva`, `diskĵokeo`
- `Wi-Fi`, `Facebook`, `Tvitero`, `evento`, `mufino`, `bovlingo`, `sprajo`
- `Ĉu mi povas/povus havi X?` 系のうち、現代会話として十分通る依頼表現
- `aliĝi al ni/vi`, `Kion ni havos por tagmanĝo/deserto?`
- `Tiel-tiel`, `dufoje pripensus`, `iri al universitato`, `vidi ... kiel`
- `doma vino`, `perdi pezon`, `havi abonon`, `fari rendevuon`
- `deklaracio`, `inkludita`, `fragila`, `poŝtejo`, `doktoro`, `kmera`, `Skajpon`
- `jaĥto / jaĥtklubo`

## 音声・モバイルデータ

修正文の音声は RHVoice `spomenka` で作成した。

生成ログ:

- `編集ログ/phrases_audio_replacement_generation_20260610_forced_loanwords.csv`
- `編集ログ/phrases_audio_replacement_generation_20260610_forced_loanwords_round2.csv`
- `編集ログ/phrases_audio_replacement_generation_20260610_forced_loanwords_round3.csv`
- `編集ログ/phrases_audio_replacement_generation_20260610_forced_loanwords_final_audit.csv`

確認結果:

- 第1ラウンド: 8件、`voice=spomenka`、全件 `generated`
- 第2ラウンド: 18件、`voice=spomenka`、全件 `generated`
- 第3ラウンド: 41件、`voice=spomenka`、全件 `generated`
- 最終検品: 4件、`voice=spomenka`、全件 `generated`
- root音声: 5000 WAV
- スマホ用音声: 5000 WAV
- `npm run validate:mobile-assets`: passed
- `npm run test:unit`: 69 tests passed

## Google Drive状態

ユーザーによる追加アップロード・旧重複削除後、`tools/build_drive_audio_manifest.py` でDriveを再読込した結果:

- Drive上の例文WAV: 5000件
- mobile data と一致する必要音声: 5000件
- missing: 0件
- extra: 0件

つまり、アプリ用に必要なDrive fallback音声はすべて揃っており、旧重複も残っていない。

## 変更された主なファイル

- `phrases_eo_en_ja_zh_ko_ru_fulfilled_260505.csv`
- `mobile_app/data/sentences.json`
- `mobile_app/data/audio_manifest.json`
- `mobile_app/app.js`
- `mobile-sw.js`
- `mobile_app/sentence-audio/*.wav`
- `Esperanto例文5000文_収録音声/*.wav`
- `編集ログ/phrases_eo_forced_loanwords_findings_20260610.md`
- 本ファイル
