# モデル契約書ver1.0 技術検証（PoC）契約書（AI）

## 想定シーン

1. **X社は、人体の姿勢推定機能を有する独自開発の学習済みモデル（ベースモデル）を保有しているAIスタートアップであり、Y社は、介護施設向けリハビリ機器の製造販売メーカーである。**
2. **X社は、秘密保持契約を締結後にY社から受領したサンプルデータを用いて検討をしたところ、自社の保有するベースモデルがY社の介護事業における見守りシステムに導入可能であるとの結論に達したので、Y社に対してその旨を根拠と共に説明した。**
3. **Y社の開発担当者は、X社のベースモデルを用いた製品開発を進めたい意向ではあるものの、今期の予算が限られていること、来期の開発予算獲得のために社内の説明資料が必要であることから、まずは技術検証（以下「PoC」という。）を行いたいとX社に伝えた。**
4. **X社とY社は、協議の結果、PoCを以下のとおり進めることを合意した。**
  1. **Y社は、X社に対し、さらなる学習用データを提供する。**
  2. **X社は、自社のベースモデルに同データを用いた学習を行うことで、より高い精度の姿勢推定を行うことができる学習済みモデル（カスタマイズモデル）のプロトタイプの生成作業や同カスタマイズモデルによる推定の精度の検証作業を実施し、検証結果を報告書にまとめて、契約締結から一定期間内にY社に提供する。**
  3. **Y社は、X社に対し、上記作業の対価として●万円を支払う。**
  4. **Y社は、X社との共同研究開発に移行するかを上記報告書の受領日から2ヶ月以内に決定する。**

## 目次

- [前文](#前文)
- [第1条（目的）](#第1条目的)
- [第2条（定義）](#第2条定義)
- [第3条（本検証）](#第3条本検証)
- [第4条（委託料および費用）](#第4条委託料および費用)
- [第5条（甲の義務）](#第5条甲の義務)
- [第6条（共同研究開発契約の締結）](#第6条共同研究開発契約の締結)
- [第7条（乙が甲に提供する資料等）](#第7条乙が甲に提供する資料等)
- [第8条（対象データの管理）](#第8条対象データの管理)
- [第9条（秘密情報）](#第9条秘密情報)
- [第10条（個人情報の取り扱い）](#第10条個人情報の取り扱い)
- [第11条（本報告書等の知的財産権）](#第11条本報告書等の知的財産権)
- [第12条（損害賠償）](#第12条損害賠償)
- [第13条（解除）](#第13条解除)
- [第14条（期間）](#第14条期間)
- [第15条（存続条項）](#第15条存続条項)
- [第16条（準拠法および管轄裁判所）](#第16条準拠法および管轄裁判所)
- [第17条（協議解決）](#第17条協議解決)
- [その他の追加オプション条項](#その他の追加オプション条項)

## 前文

　X社（以下「甲」という。）とY社（以下「乙」という。）は、甲が保有するAI技術の、乙の介護事業における見守り業務への導入可能性に関する検証（以下「本検証」という。）に関して、本契約を締結する。

### ＜ポイント＞

- 技術検証（PoC）契約は、共同研究開発段階に移行するか否かを検討する前提として、スタートアップの保有している技術の開発可能性・導入可能性などを検証するための契約である。
- 前文では、本モデル契約における検証の対象が、スタートアップが保有するAI技術のスタートアップおよび事業会社が開発対象とする製品またはサービスへの導入可能性であることを明確にしている。

### ＜解説＞

- PoC契約を締結するに当たっては、両当事者が以下に挙げる点を十分に理解することが重要である。
  1. PoC契約が将来的な共同研究開発契約の締結を目指したものであること
  2. 既に秘密保持契約を締結し、相互の情報を開示等し合った上での検証段階であること
  3. 検証においては、検証の目的を共有することが重要であり、未だ検証の目的が固まっていない場合は、まずその点を確定してからPoC契約を締結すること

### 【コラム】PoC契約の意義

- PoCは、スタートアップにとって、その技術や製品を他社に採用してもらう可能性を検討するための重要なステップである。
- もっとも、本開発への移行をちらつかされながら、次から次へと無償でPoCを依頼され、にもかかわらず本開発に移行せず、その結果、スタートアップがPoCにかかるコストを回収できないケース（いわゆる「PoC貧乏」）も散見される。「PoC貧乏」のために資金が尽きてしまうこともある。
- また、PoCの過程で得られた知見について、相手方に対して譲渡を強要されたり、無断で出願されてしまったりするなどの紛争が生じるケースもある。
- これらのことを未然に防止するための契約がPoC契約であり、AI開発の過程においては必須ともいえる契約である。

## 1条（目的）

```
第1条　本契約は、甲と乙が将来的に共同研究開発契約を締結することを視野に入れつつ、以下に定める対象技術を対象用途に対して導入・適用することの可否を判断するため（以下「本検証遂行の目的」という。）に行われる技術検証における甲と乙の権利・義務関係を定めるものである。

対象技術：甲が保有する「人体の姿勢推定AI技術」（動画・静止画から人物の姿勢をマーカーレスで推定するAI技術）

対象用途：介護施設における被介護者の見守用高機能カメラシステム（見守りカメラシステム）に利用する学習済みモデルおよび連携システムの甲乙における共同研究開発
```

### ＜ポイント＞

- 本検証遂行の目的を定める条項である。
- 秘密情報や対象データ、スタートアップが提出するレポート（本報告書）はこの目的の範囲で利用が制限される（第8条第2項、第9条第3項）。想定外の利用を防ぐために、この目的を限定的に定める必要がある。

### ＜解説＞

- 対象技術のみで「本検証遂行の目的」を特定した場合、想定している用途以外の用途への技術転用を制限できないことから、対象技術と合わせて対象用途とともに、「本検証遂行の目的」を特定する必要がある。また、対象用途の記載について、例えば、「見守りカメラシステムの開発」とだけ記載した場合、事業会社は、受領した秘密情報等を、自社独自で、あるいは他のAIスタートアップと共同して行う「見守りカメラシステムの開発」に用いることも契約上は「目的内」となるため、スタートアップは事業会社にかかる行為を禁止することはできないこととなる。そのため、対象用途においては「甲乙における共同研究開発」という限定を付すべきである。
- 事業に必須のコア技術が特許等により保護されていない限り、秘密保持契約およびPoC契約が自社の技術・ノウハウを保護する数少ない手段となる。

## 2条（定義）

```
第2条　本契約において使用される次に掲げる用語は、各々次に定義する意味を有する。

1　本検証

　第1条に定める甲の技術の導入・適用に関する技術検証をいい、具体的な作業内容は別紙1で定める。

2　対象データ

本検証に用いられる別紙2記載のデータをいう。

3　本報告書

　甲が乙に提供する、本検証に関する報告書をいう。

4　知的財産

　発明、考案、意匠、著作物その他の人間の創造的活動により生み出されるもの（発見または解明がされた自然の法則または現象であって、産業上の利用可能性があるものを含む。）および営業秘密その他の事業活動に有用な技術上または営業上の情報をいう。

5　知的財産権

　特許権、実用新案権、意匠権、著作権その他の知的財産に関して法令により定められた権利（特許を受ける権利、実用新案登録を受ける権利、意匠登録を受ける権利を含む。）をいう。

6　個人情報等

　個人情報の保護に関する法律（平成15年法律第57号）（以下「個人情報保護法」という。）に定める個人情報（同法2条1項）、個人データ（同法2条6項）および匿名加工情報（同法2条9項）をいう。

7　書面等

　書面および甲乙が書面に代わるものとして別途合意した電磁的な方法をいう。

```

### ＜ポイント＞

- 本モデル契約で使用する各用語の定義を定める条項である。
- 本検証および対象データの具体的な内容については、別紙により特定することとした。

### ＜解説＞

- 「本報告書」は、本検証の成果物であり、具体的には検証結果を記載したレポートを想定している。
- 本モデル契約のタイトルは「技術検証（PoC）契約［書］」となっているが、その実質は別紙に特定された本検証を行い、本報告書を作成することを業務とする業務委託契約（準委任契約）である。従って、本検証および本報告書の内容を一定程度詳細に特定しておかないと、後々トラブル（いつまで経っても検証がまだ終わっていないとして追加の作業や報告が発生するなど）が生じる可能性がある。そのため、別紙において、検証の作業体制・作業内容・スケジュールを含め、ある程度の詳細事項を特定する必要がある。たとえば、対象データのアノテーション作業は通常はスタートアップが行うことになるため、その点についても別紙に記載したうえでスタートアップの工数として委託料を算定することが望ましい。
- また、その前提として、事業会社がスタートアップに提供する「対象データ」の内容（データ提供者、データの項目・量、提供形式）についても、別紙にて具体的に特定しておく必要がある。
- さらに、対象データの質や量はPoCの精度に大きな影響を及ぼす。対象データは、もっぱら事業会社が収集した生データであり、その内容・量・形式については千差万別である。秘密保持契約段階で少量の対象データについてはスタートアップにおいて確認済みであろうが、PoC段階になって相当量の対象データとの提供を受けてみたところ、使い物になる質・量のデータがないということも十分にありえる。したがって、まずスタートアップとしては対象データの質がPoCの精度に大きな影響を与えることを十分に事業会社に説明をしておく必要があろう。また契約上の手当として、第3条第9項において、対象データの内容に誤り（別紙2所定のデータの項目や量を充足しない場合を含む。）があったり、提供が遅延したために、本検証の遅延や本報告書に不適合等が生じた場合にスタートアップが責任を負わない旨を定めている。
- 上記条項案では、「知的財産権」の定義として、「営業秘密およびノウハウを利用する権利」を含めていない。これは、AIの場合には特許化してそのアルゴリズムをオープンにするのではなくノウハウとして秘匿することが多いところ、 PoC後に締結する共同研究開発契約において、「知的財産権」について本モデル契約（PoC契約）と同じ定義を用いた上で、同「知的財産権」について事業会社に移転する旨の条項が入ると、スタートアップのノウハウおよび営業秘密を利用する権利までもが事業会社に移転すると解釈されるおそれがあるためである。
- 本モデル契約書上、重要な通知等は書面等の記録に残る形で行うことを要求している（例えば、第3条第4項所定の本報告書に対する異議など）。しかし、契約締結自体をも電子的に行われつつある今般、重要な通知等といえども、それに厳格な書面性を要求することは必ずしも適当でない。そこで、かかる通知等は書面の他、当事者間で別途合意した電子的な方法で行うことも可能としている。具体的には電子メール等を想定している。

## 3条（本検証）

```
第3条　乙は、甲に対し、本検証の実施を依頼し、甲はこれを引き受ける。

2　乙は、甲に対し、対象データを本契約締結後●日以内に提供する。甲は、受領したデータを確認した上で、乙に対しその旨を速やかに通知する。

3 甲は、前項の通知が乙に到達した後●日以内に、乙に対し、本報告書を提供する。

4　本報告書の提出後、乙が、甲に対し、本報告書を確認した旨を通知した時または乙が具体的な理由を明示して書面等で異議を述べることなく1週間が経過した時に、乙による本報告書の確認が完了したものみなす。本報告書の確認が完了した時点をもって、甲による本検証にかかる義務の履行は完了する。

5　乙は、甲に対し、本報告書提出後1週間が経過するまでの間に前項の異議を述べた場合に限り、本報告書の修正を求めることができる。

6　前項に基づき、乙が本報告書の修正を求めた場合、甲は、速やかにこれを修正した本報告書を改めて提出し、乙は、再度それを確認する。再確認については、本条第4項および第5項を準用する。

7 乙は、甲に対し、対象データを甲に提供することについて、正当な権限があることおよびかかる提供が法令に違反するものではないことを保証する。

8　乙は、対象データの正確性、完全性、有効性、有用性および安全性等について保証しない。ただし、本契約に別段の定めがある場合はその限りでない。

9　乙が甲に対し提供を行った対象データの内容に誤り（別紙2所定のデータの項目や量を充足しない場合を含む。以下同じ。）があった場合またはかかる提供を遅延した場合、甲は、これらの誤りまたは遅延によって生じた本検証の遅延または本報告書の不適合等の結果について責任を負わない。

10　甲は、対象データの正確性、完全性、有効性、有用性および安全性等について、確認・検証の義務その他の責任を負うものではない。
```

### ＜ポイント＞

- スタートアップが担当する業務が本検証であることを定めている。
- 本モデル契約で想定している検証（本検証）は、事業会社が提供するデータを用いて対象技術の導入・適用による開発の可否や妥当性の評価を行うことである。
- 本検証は、一定の成果物の完成を目的としたもの（請負型）ではなく、検証のための業務の実施を目的としたもの（準委任型）である。

### ＜解説＞

- 事業会社から対象データの提供を受けない限り、当然、スタートアップにおいて検証業務を開始することはできない。しかし、実際にPoCを推進するにあたっては、事業会社においてデータ提供の準備が整っていないことも多く、その結果、スタートアップが事業会社からデータの提供を受けられず検証作業に着手できないということが度々発生する。そこで、本モデル契約では、事業会社からのデータ提供期限を第2項において明記するとともに、第3項において、事業会社のデータ提供期限とスタートアップの報告書の提出期限をリンクさせている。
- また、本報告書の提供後、いつまでも本検証の追加作業を依頼されるというトラブルを防ぐために報告書の確認（本検証の完了）の期限を定める規定（第4項）を設けることがポイントとなる。
- 確認の期限は、本報告書の内容が必要な内容を満たしているかを確認するための期間である。適切な期間は本検証の内容によっても異なるが、通常は1週間程度が妥当と考えられる（第5項）。
- 事業会社が提供する対象データの内容をスタートアップは契約締結時には把握していないため、前述のように、検証が始まって実際に対象データの提供を受けてみたところ、検証に利用できるだけの質・量のデータが存在しなかったということがある。また、対象データが事業会社において迅速にスタートアップに提供できる体制で管理されていないため、対象データの提供が大幅に遅延することも時にみられる。そのような場合に、検証が遅延し、あるいは検証内容に不備が生じたとしてもスタートアップにその責任を負わせるのは不合理である。そこで、本条では、対象データの内容に誤り（別紙2所定のデータの項目や量を充足しない場合を含む。）があったり、提供が遅延したために、本検証の遅延や本報告書に不適合等が生じた場合にスタートアップが責任を負わない旨を定めている（第9項）。
- なお、PoC段階であるにもかかわらず、事業会社での検証のために必要である等の理由でPoCにおいてスタートアップが生成した学習済みモデルのプロトタイプのソースコードの引き渡しを事業会社が要請することがある。しかし、前文の解説にも記載したとおり、PoCの目的は、共同研究開発段階に移行するか否かを判断する前提として、スタートアップの保有している技術の開発可能性・導入可能性などを検証することにある。したがって、PoC契約において、学習済みモデルのソースコードを、仮に検証目的だとしても引き渡し対象とすることはPoC契約の目的を超えるものであり不合理である。次段階への移行の可否については、検証結果の報告書のみで判断可能なのであって、仮に報告書だけでは判断できないのであれば、それは報告書に盛り込むべき項目に不足があったということを意味しているに過ぎない。さらに、PoC段階においてソースコードを引き渡すということは、当該ソースコードの流出や他目的での利用等、スタートアップにとって致命的な事態を招くリスクが大きい。したがって、スタートアップとしては、PoC段階において学習済モデルのソースコードを引き渡すことは名目の如何を問わず避けることが望ましい。

## 4条（委託料および費用）

```
第4条　本検証の委託料は●万円（税別）とし、以下のとおり分割し、甲が指定する金融機関の口座に振込送金する方法により支払う。振込手数料は乙の負担とする。

①　本契約締結後10日以内

　　●万円（税別）

②　本報告書の乙による確認の完了日から1ヶ月以内

　　●万円（税別）
```

### ＜ポイント＞

- 本モデル契約における業務の対価としての委託料の金額、支払時期および支払方法を定める条項である。
- 委託料については、本条のように固定金額とする他に、人月単位または工数単位に基づく算定方法のみ規定し、毎月の委託料を算定する方法とすること等が考えられる。

### ＜解説＞

- 委託料の支払方法としては、①一定の時期に一括して支払う方式、②着手時および本報告書の確認完了時等に分割して支払う方式、③一定の業務時間に達するごとに当該業務時間分の対価を支払う方式等様々な方式がある。
- 本モデル契約では②の方式を採用している。

###【4条：変更オプション　－　共同研究開発契約を締結した場合に委託料を一部免除】

```
第4条　本検証の委託料は●万円（税別）とし、以下のとおり分割し、甲が指定する金融機関の口座に振込送金する方法により支払う。振込手数料は乙の負担とする。但し、③については、本報告書の乙による確認の完了日から4か月以内に共同研究開発契約が締結された場合は免除されるものとする。

①　本契約締結後10日以内

　　●万円（税別）

②　本報告書の乙による確認の完了日から1ヶ月以内

　　●万円（税別）

③　本報告書の乙による確認の完了日から5ヶ月以内

　　●万円（税別）
```

#### ＜解説＞

- 事業会社としては、PoC段階をあくまで共同研究開発段階の前段階と認識しているため、委託料を低額に抑えるという判断になることも多い。
- スタートアップとしては、共同研究開発に進めるのであれば、PoC段階では低額な委託料に甘んじるという方針もあり得る。
- そこで、これらの思惑の調整規定として、共同研究開発契約が締結された場合とされなかった場合で支払われるべきPoC費用に差を設けることが考えられる。同契約が締結された場合には費用を一部免除するという構成と、同契約が締結されなかった場合に限り追加の費用を支払うという構成が考えられるところ、本変更オプションは前者を採用したものである。
- 本モデル契約第6条第2項では、事業会社は、本報告書の確認の完了日から2ヶ月以内に、スタートアップに対して共同研究開発に進むか否かの検討結果を通知することとしている。本変更オプションでは、当該通知がなされてから実際に共同研究開発契約が締結されるまでの時間（契約交渉の時間）を2ヶ月と想定し、本報告書の事業会社による確認の完了日から4ヶ月（2ヶ月+2ヶ月）以内に同契約が締結された場合に費用の一部（③の費用）を免除することとしている。

## 5条（甲の義務）

```
第5条　甲は、善良なる管理者の注意をもって本検証を遂行する義務を負う。ただし、前条第1号に定める委託料の支払を受けるまでは、甲は本検証に着手する義務を負わず、また本契約を遂行しなかったことによる責めを負わない。

2　甲は、本検証に基づく何らかの成果の達成や特定の結果等を保証するものではない。
```

### ＜ポイント＞

- 本検証を履行するに際してのスタートアップの法的義務および結果に対する非保証を定めた条項である。

### ＜解説＞

- PoC契約の法的性質は準委任契約であることから、スタートアップが善管注意義務を負うことを確認するとともに（第1項）、スタートアップが何らかの成果の達成義務を負うものではないことも明確にしている（第3項）。
- また、AI技術の性質上、目指している結果が出ない場合、その原因が提供されたデータにあるのか、AI技術のアルゴリズムや学習方法等にあるのか不明確なことも多いことに鑑み、スタートアップの義務として特定の結果の保証も行わないことも明確にしている。

## 6条（共同研究開発契約の締結）

```
第6条　甲および乙は、本検証が対象技術を対象用途に対して導入・適用することの可否の判断を目的とするものであることに鑑み、その実効性が確認された場合には、共同研究開発への移行の決定に向けて速やかに協議を開始する。

2　乙は、本報告書の確認の完了日から2ヶ月以内に、甲に対して共同研究開発に進むか否かの検討結果を通知する。
```

### ＜ポイント＞

- 共同研究開発契約への移行についての規定である。

### ＜解説＞

- PoCは、共同研究開発への移行のための実証段階という性質を有していることから、当事者に共同研究開発契約締結に向けた協議義務（努力義務）を課している。
- また、PoC後に次のステップに進むかどうか未確定なままで時間が経過することを避けるため、事業会社に対し一定期間内に共同研究開発契約を締結するか否かの通知義務を課している。

## 7条（乙が甲に提供する資料等）

```
第7条　乙は、甲に対し、本検証に合理的に必要なものとして甲が要求し、乙が合意した資料、機器および設備等（以下「資料等」という。）の提供、開示および貸与等（以下「提供等」という。）を行う。

2　第3条第7項ないし第10項の規定を、乙が甲に対し資料等を提供等することについて準用する。
```

### ＜ポイント＞

- 本検証に際して、事業会社による資料等の提供および提供された資料等に起因する責任について取り決めた規定である。対象データの提供にかかる規定と同様の規定となることから、該当する条項を準用している。

## 8条（対象データの管理）

```
第8条　甲は、対象データを、善良な管理者の注意をもって管理、保管し、乙の事前の書面等による承諾を得ずに、第三者に開示、提供または漏えいしてはならない。

2 甲は、対象データについて、事前に乙から書面等による承諾を得ずに、本検証遂行の目的以外の目的で使用、複製および改変してはならず、本検証遂行の目的に合理的に必要となる範囲でのみ、使用、複製および改変できる。

3 甲は、対象データを、本検証遂行のために知る必要のある自己の役員および従業員に限り開示等するものとし、この場合、本条に基づき甲が負担する義務と同等の義務を、開示等を受けた当該役員および従業員に退職後も含め課さなければならない。

4 甲は、対象データのうち、法令の定めに基づき開示等すべき情報を、可能な限り事前に乙に通知した上で、当該法令の定めに基づく開示先に対し開示等することができる。

5 本検証の完了後、乙が甲に対し、第6条に基づき、共同研究開発契約を締結しない旨を通知した場合または乙の指示があった場合、甲は、乙の指示に従って、対象データ（複製物および同一性を有する改変物を含む。）が記録された媒体を破棄もしくは乙に返還し、かつ、甲が管理する一切の電磁的記録媒体から削除する。なお、乙は甲に対し、対象データの破棄または削除について証明する文書の提出を求めることができる。

6 甲は、本契約に別段の定めがある場合を除き、乙による対象データの提供は、乙の知的財産権を譲渡、移転、利用許諾するものでないことを確認する。

7 本条の規定は、前項を除き、本契約が終了した日より3年間有効に存続する。
```

### ＜ポイント＞

- 本検証に際して、事業会社がスタートアップに提供した対象データの管理等について定めた規定である。

### ＜解説＞

- 本検証のために事業会社からスタートアップに提供された対象データについては、一般的な秘密情報とは異なる別途の考慮が必要となる場合が多いと考えられるため、一般的な秘密情報に関する規定（第9条）と異なる規定を本条で設けている。
- 本条の対象は「対象データおよび資料等」ではなく「対象データ」のみであり、対象データに含まれない「資料等」については、秘密情報の取扱いを定める第9条での保護対象となる。
- 本モデル契約が想定するPoC段階では、検証目的で一定の対象データを受領する場合を前提としているため、利用契約と異なり対象データの目的外利用を認める規定は設けていない。本条は、存続条項があるため（第7項）、本モデル契約の終了後も3年間効力を有する。ただし、第7項に、「前項を除き」と規定されていることから、第6項の規定については、原則（第15条）に戻り、期間の定めなく効力を有することになる。

## 9条（秘密情報）

```
第9条　甲および乙は、本検証遂行の目的のため、文書、口頭、電磁的記録媒体その他開示等の方法ならびに媒体を問わず、また、本契約の締結前後にかかわらず、甲または乙が相手方（以下「受領者」という。）に開示等した一切の情報（本報告書に記載された情報を含み、対象データを除く。以下「秘密情報」という。）を秘密として保持し、秘密情報を開示等した者（以下「開示者」という。）の事前の書面等による承諾を得ずに、第三者に開示または漏洩してはならない。

2　前項の定めにかかわらず、次の各号のいずれか一つに該当する情報については、秘密情報に該当しない。

 1.  開示者から開示等された時点で既に公知となっていたもの
 2.  開示者から開示等された後で、受領者の帰責事由によらずに公知となったもの
 3.  正当な権限を有する第三者から秘密保持義務を負わずに適法に開示等されたもの
 4.  開示者から開示等された時点で、既に適法に保有していたもの
 5.  開示者から開示等された情報を使用することなく独自に取得または創出したもの

3　受領者は、秘密情報について、事前に開示者から書面等による承諾を得ずに、本検証遂行の目的以外の目的で使用、複製および改変してはならず、本検証遂行の目的に合理的に必要となる範囲でのみ、使用、複製および改変できる。

4　受領者は、秘密情報を、本検証遂行のために知る必要のある自己の役員および従業員（以下「役員等」という。）に限り開示等するものとし、この場合、本条に基づき受領者が負担する義務と同等の義務を、開示等を受けた当該役員等に退職後も含め課す。

5　本条第1項、同条第3項および第4項の定めにかかわらず、受領者は、次の各号に定める場合、可能な限り事前に開示者に通知した上で、当該秘密情報を開示等することができる。

1.  法令の定めに基づき開示等すべき場合
2.  裁判所の命令、監督官公庁またはその他法令・規則の定めに基づく開示等の要求がある場合

3.  受領者が、弁護士、公認会計士、税理士、司法書士等、秘密保持義務を法律上負担する者に相談する必要がある場合

6　本条第1項、同条第3項および第4項の定めにかかわらず、甲および乙は、相手方の事前の承諾なく、以下の事実を第三者に公表することができる。

　　甲乙間で、本検証が開始された事実

7　本検証が完了した場合、本契約が終了した場合または開示者の指示があった場合のいずれかに該当する場合、受領者は、開示者の指示に従って、秘密情報（その複製物および同一性を有する改変物を含む。）が記録された媒体、ならびに、未使用の素材、機器およびその他有体物を破棄もしくは開示者に返還し、かつ、受領者が管理する一切の電磁的記録媒体から削除する。なお、開示者は受領者に対し、秘密情報の破棄または削除について証明する文書の提出を求めることができる。

8　受領者は、本契約に別段の定めがある場合を除き、秘密情報により、開示者の知的財産権を譲渡、移転または利用許諾するものでないことを確認する。

9　本条は、秘密情報に関する甲乙間の合意の完全なる唯一の表明であり、秘密情報に関する甲乙間の書面等または口頭による提案およびその他の連絡事項の全てに取って代わる。

10　本条の規定は、第8項を除き、本契約が終了した日より3年間有効に存続する。
```

### ＜ポイント＞

- 相手から提供を受けた秘密情報の管理方法に関する条項である。

### ＜解説＞

秘密情報の定義

- 秘密情報の定義については、当事者間でやりとりされる情報を包括的に対象とする場合と、個別に秘密である旨の特定を要求する場合があるが、簡易迅速に行うことが多いPoC段階において、秘密である旨の特定を忘れることによるリスクを避けるため、秘密保持契約における秘密情報の定義と異なり前者の規定を原則とした。なお、対象データについてはその管理方法について第8条で定めているため秘密情報の定義から除外している。
- 他方で、秘密情報を「一切の情報」と包括的に定義すると、範囲が広過ぎるとして有効性が争われ、逆に保護の範囲が狭まってしまう（秘密情報とは保護に値する情報を意味すると限定解釈される）リスクが発生する。このリスクを排除するためには、秘密を指定する条文を採用すればよい。
- なお、秘密を指定する条文オプションとその背景となる秘密情報の範囲に関する考え方については、モデル契約（新素材）の「秘密保持契約」に詳細に解説しているため、そちらを参考にされたい。

### 【コラム】秘密情報管理の詳細については以下も参照されたい。

- 秘密情報の保護ハンドブックの手引き
  - <https://www.meti.go.jp/policy/economy/chizai/chiteki/pdf/170607\_hbtebiki.pdf>
- 秘密情報の保護ハンドブック
  - <https://www.meti.go.jp/policy/economy/chizai/chiteki/pdf/handbook/full.pdf>
- 知財を使った企業連携4つのポイント
  - <https://www.meti.go.jp/policy/economy/chizai/chiteki/pdf/170607\_hbtebiki.pdf>

技術検証が開始された事実の公表

- スタートアップにとって重要な条項となるのが本条第6項である。スタートアップにとって、自社技術が事業会社への導入の技術検証（PoC）の段階まで進んだとの事実は、投資家やユーザーに対する効果的なPR材料になる場合が多く、スタートアップがかかる事実の公表を望むケースが多い。
- しかし、本条第6項のような規定が入っていない場合、秘密情報の定義の内容によっては、かかる事実の第三者への公表が秘密保持義務違反を構成するか否かが曖昧なケースも存在し、スタートアップが公表に踏み切れないケースや、事業会社に事前に許可を求めるも社内決裁を得るのに時間がかかり発表すべきタイミングに発表できないケースも散見される。
- そこで、本モデル契約においては、スタートアップ-事業会社間で本検証が開始された事実は公表しても問題ないと合意できたと想定し、公表を積極的に許可する規定を設けることで、かかる弊害を回避することとした。

秘密保持契約とPoC契約内の秘密保持条項の関係

- 秘密保持契約に引き続いてPoC契約を締結する場合、秘密保持契約とPoC契約内の秘密保持条項の関係が問題となる。
- PoC契約において秘密保持条項を設けず、前者が引き続き適用されるとすることもあるが、本モデル契約においては、秘密保持契約の締結時点よりも、秘密情報の対象について具体的な情報整理が進んでいると想定し、本モデル契約内の秘密保持条項が、すでに締結されている秘密保持契約を上書きすることを第9項で明記している。

> この点について、すでに締結した秘密保持契約の内容を本モデル契約で上書きすることで齟齬が生じないか、十分に注意して規定する必要がある。

PoC段階における秘密保持条項の必要性

- PoC段階など、相手方から提供を受けた秘密情報と並んで、検証結果などの成果物情報が存在する場合、これらの成果物情報（いわゆるフォアグラウンド情報）も秘密保持の対象とする必要がある。すでに秘密保持契約を締結している場合も多いと思われるが、秘密保持契約のみでは秘密情報の定義上、フォアグラウンド情報が含まれるかどうかが曖昧なケースが多いため、別途PoC契約で秘密保持契約条項を設ける必要がある。

## 10条（個人情報の取り扱い）

```
第10条　本検証遂行に際して、乙が個人情報等を含んだ対象データを甲に提供する場合には、個人情報保護法に定められている手続を履践していることを保証するものとする。

2　乙は、本共同開発の遂行に際して、個人情報等を含んだ対象データを甲に提供する場合には、事前にその旨を明示する。

3　甲は、第 1 項に従って個人情報等が提供される場合には、個人情報保護法を遵守し、個人情報等の管理に必要な措置を講ずるものとする。
```

### ＜ポイント＞

- 対象データおよび資料等に個人情報等が含まれる場合に関する規定である。

### ＜解説＞

- システムの構想段階から個人情報保護のための方策を作り込むことを、プライバシー・バイ・デザイン（Privacy by Design：PbD）といい、事後のプライバシー侵害のリスクを低減する効果的な手段とされる。この考え方に従い、PoCを設計する時点で、どのようなデータが提供され得るのかを検討し、それに応じた法令上の具体的な義務を履践すべきことを条項化して義務付けることが望ましい。

### 11条（本報告書等の知的財産権）

```
第11条　本報告書および本検証遂行に伴い生じた知的財産権（著作権法27条および28条の権利を含む。）は、乙または第三者が従前から保有しているものを除き、甲に帰属するものとする。

2　甲は、乙に対し、本検証遂行の目的に必要な範囲に限り、乙自身が本報告書を使用、複製および改変することを許諾する。

3　乙は、自らの負担と責任により、本報告書の使用、複製および改変、ならびに当該複製等により作成された複製物等の使用等を行う。甲は、乙に対し、本契約で別段の定めがある場合または甲の責に帰すべき事由がある場合を除いて、乙による本報告書の使用等により乙に生じた損害を賠償する責任を負わない。

4　甲は、乙に対し、本契約に従った本報告書の利用について、著作者人格権を行使しない。
```

### ＜ポイント＞

- 本報告書および本検証遂行に伴い生じた知的財産権の取扱いおよび利用条件について取り決めている。

### ＜解説＞

本報告書および本検証遂行に伴い生じた知的財産権の帰属

- 本報告書であるレポートや、その他本検証の過程で生じる知的財産権の取扱いについては、スタートアップ・事業会社間で争いが生じることがあるので、契約において規定しておくことが重要である。
- 本モデル契約では本検証の作業主体がスタートアップであること、検証段階においては、報告書を利用できれば導入可否の検討という目的を達成できると考えられることから、本報告書および本検証遂行に伴い生じた知的財産権はすべてスタートアップに帰属することと規定している。
- なお、報告書の著作権について、スタートアップから事業会社に移転するよう求める事業会社が散見されるが、そのような要求をされるとスタートアップとしては、報告書の記載内容をなるべく簡略化しようというインセンティブが発生することになり、事業会社にとってのデメリットが大きい。また報告書の著作権を移転させることは、同報告書の記載について著作権法上の利用行為（複製等）ができるということを意味するに過ぎないが、事業会社から見た場合、上記のような報告書内容の簡略化というデメリットを甘受してもなお、著作権の移転を受ける必要性があるか疑問がある。したがって、報告書の著作権については、むしろ事業会社の利益のためにも、スタートアップに留保する扱いとすべきである。
- 本報告書の利用が第三者の知的財産権を侵害しないことの保証を求められる場合もあるが、PoC段階では最終的に完成させるべき成果物が定まっていないため、第三者の知的財産権の侵害の有無を判断する前提となる事実関係が固まっておらず、侵害の有無の確認が困難であること等を踏まえ、本モデル契約では保証条項は設けないこととした。

技術検証段階におけるスタートアップと事業会社の関係性

- 事業会社としては、委託料を払っている以上、本報告書を含むすべての知的財産権は事業会社に帰属すべきと考えるかもしれない。しかしながら、PoC契約における委託料は、原則としてスタートアップの検証作業に対する対価であり、検証作業にて発生した知的財産権の譲渡を受けるためには、別途それに見合う対価をスタートアップに支払う必要がある。
- 事業会社は、オープンイノベーションを通じて自社の事業を加速させるという観点から、スタートアップとの間で適切な知的財産権の分配を行うことの重要性を意識した上で、PoC段階において最も重要なのは共同研究開発の実現に向けた報告書の内容であり、その知的財産権の帰属ではないことを認識されたい。

### 【追加オプション － フィードバック規定】

```
> **　**本検証遂行の過程で、乙が甲に対し、本検証に関して何らかの提案や助言を行った場合、甲はそれを無償で、甲の今後のサービスの改善のために利用することができる。当該提案や助言が秘密情報に該当する場合、乙は甲による当該利用について、本契約の締結をもって本契約9条3項に定める承諾をおこなうものとする。
```

#### ＜解説＞

- 本検証において、事業会社からスタートアップに対し提案や助言（フィードバック）が行われることも多いが、フィードバックの利用条件に関して後にトラブルが発生しないようにするため、これらの利用についてオプション条項のように規定しておくことも考えられる。
- オプション条項ではフィードバック規定の対象を「何らかの提案や助言」とし、それらを利用できる目的の範囲を「甲の今後のサービスの改善のため」と、いずれも広く定義しているが、いずれも、スタートアップと事業会社間の交渉により、対象をより詳細に、あるいは利用目的の範囲を狭く定義することも考えられる。
- なおフィードバック規定の対象である「何らかの提案や助言」が、第9条における「秘密情報」に該当することもあり得ると思われる。そのため、それらの提案や助言の、利用目的の範囲における利用が秘密情報の目的外利用の禁止（第9条第3項）における承諾対象であることを明記した。もっとも、承諾の対象となっているのは目的外利用の禁止（第9条第3項）のみであるため、第三者開示の禁止（第9条第1項）はそのまま適用され、仮に本オプション条項を締結したとしても、スタートアップは事業会社から提供された「何らかの提案や助言」を第三者に開示することはできない。
- また、「何らかの提案や助言」について事業会社が何らかの知的財産権（特許権等）を保有していることがありうる。その場合、当該提案や助言の利用は当該知的財産権の実施に該当することがありうるが、その点については、本オプション条項が第9条第8項に規定する「別段の定め」に該当することによって許容されることとなる。

### 12条（損害賠償）

```
第12条　乙は、甲の責めに帰すべき事由により損害を被った場合、甲に対して損害賠償を請求することができる。ただし、甲が乙に対して本契約に関して負担する損害賠償責任の範囲は債務不履行責任、知的財産権の侵害、不当利得、不法行為責任、その他法律上の請求原因の如何を問わず、乙に現実に発生した直接かつ通常の損害に限られ、逸失利益を含む特別損害は、甲の予見または予見可能性の如何を問わず甲は責任を負わない。

2　前項に基づき甲が乙に対して損害賠償責任を負う場合であっても、本契約の委託料を上限とする。

3　前2項は、甲に故意または重大な過失がある場合は適用されない。
```

### ＜ポイント＞

- 契約の履行に関して契約違反が生じた場合の違反行為の停止等および損害賠償責任に関する条項である。

### ＜解説＞

- 損害賠償責任の範囲・金額・請求期間については、本検証の内容やコストの負担、委託料の額等を考慮してスタートアップ・事業会社の合意によりあらかじめ定めるケースもあるが、本条では具体的な損害賠償額は定めず、その上限のみ定めた。
- 本モデル契約では、スタートアップの損害賠償責任の範囲について、何を請求原因とするのかにかかわらず、損害賠償額の上限は本モデル契約（本検証）の委託料を限度とすることを定めている。
- 但し、故意・重過失の場合には、上限規定は適用されないものとしている。損害発生の原因が故意による場合には、免責・責任制限に関する条項は無効になると解釈されるおそれがあり、故意に準ずる重過失の場合（例えば、重大な情報の漏洩等）にも同様に無効とするのが有力な考え方であることから、このような規定を設けた。

### 13条（解除）

```
第13条　甲または乙は、相手方に次の各号のいずれかに該当する事由が生じた場合には、何らの催告なしに直ちに本契約の全部または一部を解除することができる。

1.  本契約の条項について重大な違反を犯した場合

2.  支払いの停止があった場合または競売、破産手続開始、民事再生手続開始、会社更生手続開始、特別清算開始の申立てがあった場合

3.  手形交換所の取引停止処分を受けた場合

4.  本報告書および本検証遂行に伴い生じた知的財産権の有効性を争った場合

5.  その他前各号に準ずるような本契約を継続し難い重大な事由が発生した場合

2　甲または乙は、相手方が本契約のいずれかの条項に違反し、相当期間を定めてなした催告後も、相手方の債務不履行が是正されない場合は、本契約の全部または一部を解除することができる。
```

### ＜ポイント＞

- 契約解除に関する一般的規定である。

### ＜解説＞

- スタートアップとしては、以下のようないわゆるチェンジオブコントロール条項（COC条項）等により、M&Aが本モデル契約の解除事由として定められると、M&Aに先立つデューデリジェンスにおいてリスクとして評価されうる。

####【解除事由としてのCOC条項の例】

他の法人と合併、企業提携あるいは株主の大幅な変動により、経営権が実質的に第三者に移動したと認められた場合

#### ＜解説＞

- かかる条項が解除事由に含まれている場合は、これらの支障を説明した上で削除を求めることも検討を要する。
- 事業会社より、スタートアップが競合企業に吸収合併されて秘密情報が競合にわたってしまうことを懸念してCOC条項の導入が求められる場合も考えられる。
- その場合には、当該懸念を解消するべく、解除事由となる経営権の移転先を競合会社（具体的に会社名を列挙することも考えられる。）に限定した上でCOC条項を導入することも考えられる。

## 14条（期間）

```
第14条　本契約は、本契約の締結日から6ヶ月または乙による本報告書の確認の完了日のいずれか早い日まで効力を有する。
```

### ＜ポイント＞

- 契約の有効期間を定めた一般的な条項である。

### ＜解説＞

- 本モデル契約では、本報告書の確認の完了日（第3条第4項）を基準に有効期間を定めることとしつつも、事業会社が確認をしない限り、いつまでも契約が続いてしまうことが想定されることから、最長でも6ヶ月を超えないこととしている。

## 15条（存続条項）

```
第15条　本契約が期間満了または解除により終了した場合であっても本契約第3条（本検証）第7項から第10項、第5条第2項（甲の義務）、第6条（共同研究開発契約の締結）、第7条（乙が甲に提供する資料等）第2項 、第8条（対象データの管理）から第12条（損害賠償）、本条、第16条（準拠法および管轄裁判所）ならびに第17条（協議解決）の定めは有効に存続する。
```

### ＜ポイント＞

- 契約終了後も効力が存続すべき条項に関する一般的規定である。

## 16条（準拠法および管轄裁判所）

```
第16条　本契約に関する一切の紛争については、日本法を準拠法とし、●地方裁判所を第一審の専属的合意管轄裁判所とする。
```

### ＜ポイント＞

- 準拠法および紛争解決手続きに関して裁判管轄を定める条項である。

### ＜解説＞

- クロスボーダーの取引も想定し、準拠法を定めている。
- 紛争解決手段については、上記のように裁判手続きでの解決を前提に裁判管轄を定める他、調停や仲裁によるとする場合もある。

## 17条（協議解決）

```
第17条　本契約に定めのない事項または本契約の解釈についての疑義が生じた場合、甲乙にて協議の上、解決する。
```

### ＜ポイント＞

- 紛争発生時の一般的な協議解決の条項である。

## その他の追加オプション条項

### 再委託

```
第●条　甲は、乙が書面等によって事前に承認した場合、本検証にかかる業務の一部を第三者（以下「委託先」という。）に再委託することができる。なお、乙が上記の承諾を拒否するには、合理的な理由を要する。

2　前項の定めに従い委託先に本検証にかかる業務の一部を委託する場合、甲は、本契約における自己の義務と同等の義務を、当該委託先に課す。

3　甲は、委託先による業務の遂行について、乙に帰責事由がある場合を除き、自ら業務を遂行した場合と同様の責任を負う。ただし、乙の指定した委託先による業務の遂行については、甲に故意または重過失がある場合を除き、責任を負わない。
```

#### ＜ポイント＞

- 本検証にかかる業務の再委託の可否および再委託がなされた場合のスタートアップの責任について定める条項である。

#### ＜解説＞

- 再委託の可否については、再委託について事業会社の事前承諾を要するパターンと再委託先の選定について原則としてスタートアップの裁量により行えるパターンが考えられる。
- 技術検証（PoC）においては、スタートアップ自身の技術力に着目して契約が締結されることや、事業会社が提供する資料等の取扱いについて事業会社のコントロールを及ぼすという観点から、本モデル契約では、再委託について事業会社の事前同意を必要としている。

### 契約内容の変更**

```
第●条　本検証の対象が想定外に拡大した等の事情により、検証期間、委託料等の契約条件の変更が必要となった場合、甲または乙は、相手方に当該変更の要否についての協議を書面等で申し出るものとし、当該申し出を受けた当事者は、速やかに当該協議に応じるものとする。
2　前項の協議に基づき、本契約の内容の一部変更をする場合、甲および乙は、当該変更内容が記載された変更契約を書面等で締結する。
```

#### ＜ポイント＞

- 想定外の事態が生じた場合に、契約内容の変更について協議をすることおよび契約内容を変更することとなった場合の手続について定める条項である。

### 権利義務の譲渡の禁止

```
第●条　甲および乙は、互いに相手方の事前の書面等による同意なくして、本契約上の地位を第三者に承継または本契約から生じる権利義務の全部もしくは一部を第三者に譲渡し、引き受けさせもしくは担保に供してはならない。
```

#### ＜ポイント＞

- 契約上の地位については相手方の承諾なく譲渡できないとする一般的な規定である。

```
本契約締結の証として、本書2通を作成し、甲、乙記名押印の上、各自1通を保有する。
```

　　　　年　　月　　日

甲

乙

---

（別紙1：本検証）

\(1\) 作業体制

　●

\(2\) 作業内容および役割分担

【記載例】

ア　甲

　①　対象データにアノテーションを行うことによる学習用データセット作成

　②　甲が本契約締結前から保有する学習済みモデルに学習用データセットを用いた学習を行うことによる学習済モデルのプロトタイプの生成・精度向上

　③　②で生成したプロトタイプを用いた姿勢推定精度の評価および当該評価を踏まえた本報告書の作成

イ　乙

　①　対象データの収集及び甲への提供

　②　ア③の評価に対する協力

\(3\) 検証期間

　●

---

（別紙2：対象データ）

(1)データの概要

（例）介護施設に乙がカメラを設置したうえで撮影した動画データ。当該動画データについては、乙において個人情報が含まれない形に匿名加工を行うか、あるいは撮影対象である被介護者本人から第三者提供に関する同意を取得するなど個人情報保護法上に定められている手続を履践するものとする。

(2)データの項目

(3)データの量

(4)データの提供形式

