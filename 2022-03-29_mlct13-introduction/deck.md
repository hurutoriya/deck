---
marp: true
class: invert
paginate: true
---

# <!--fit--> Machine Learing Casual Talks #13

テーマ: 「Human In The Loop」🧐 🤝 🤖

https://mlct.connpass.com/event/239953/

2022/03/30 20:00~

🐦 Twitter ハッシュタグ: [#MLCT](https://twitter.com/hashtag/MLCT)

---

# <!--fit--> [Machine Learning Casual Talks をはじめた理由](https://docs.google.com/presentation/d/1-a41qyXdB1E2yheJNK29g0Ty88COdFQ1IJRs6uqSe_Y/edit#slide=id.p)

🇨🇦 [バンクーバーにいる @chezou さん](https://chezo.uno/post/2021-12-18-8-months-after-relocating-vancouver/)に変わって説明

---

# アンチハラスメントポリシー 👮

ハラスメントとは、性差、性同一性と表現、性的指向、障害、外見や身体的特徴、人種、宗教、公共な場での性的な画像や類する表現、脅迫、ストーカ、望まない写真撮影や録音・録画、不適切な接触、およびそれらに関連した不快な言動が含まれます

MLCT では全ての参加者がナレッジ共有に集中できるよう、これらのハラスメント行為を許容しません
MLCT イベントだけでなく、MLCT の内容や状況についてブログや SNS などで公開、コメントなどいただく際にも、これらハラスメント行為がないようご留意ください
万が一、ハラスメント行為を見聞きした参加者は、お手数ですが MLCT の窓口を行っている所（@hurutoriya）まで Twitter DM などでご一報ください

---

# <!--fit--> カジュアルの定義

# カジュアルトークを開くと、その手の人がカジュアルに自分の好きなことばっかり話すからガチな話しかない

---

# MLCT の狙い

- 論文にはあまり出ない実務で得たノウハウの共有
- 機械学習実用のための`生きた知識`を暗黙知から公開知へ

---

# で、司会やっている人誰?

- 上田隼也 🦅 @hurutoriya
- 検索エンジニア 株式会社メルカリ
  - 2021 年に機械学習エンジニアから検索エンジニアに転生
- MLCT を 2018 年に一度復活させ、育児で 2 年間休止していましたが、戻ってまいりました
- 2 年前に業務の成果を Human In The Loop を取り扱った MLOps の国際会議論文として書いたので、興味のある人は見てね

[Auto Content Moderation in C2C e-Commerce](https://www.usenix.org/conference/opml20/presentation/ueta)

---

## 今回のテーマ: Human In The Loop について 🧐 🤝 🤖

> Q. より良いモデルを効率的に学習するために人間をどう活用するか?

_馬場先生の[ Human-in-the-Loop 機械学習](https://speakerdeck.com/yukinobaba/human-in-the-loop-machine-learning) より抜粋_

少し広めの具体例として、

- 効率的なアノテーションについて(能動学習, アノテーション環境など)
- 高品質なデータを手に入れるための取り組み

などで今回は募集させていただきました

---

# 登壇者紹介

各発表者への質問は sli.do で募集します

各登壇者が発表中に sli.do での質問の投稿をお願いします
各登壇者の質疑応答が終わるごとに その登壇者への sli.do での質問はアーカイブしていきます

sli.do event code: `mlct13`

---

# 石原祥太郎

- `20:05-20:30`: 発表
- `20:30-20:35`: 質疑応答

登壇テーマ

「Editors-in-the-loop なニュース記事要約システムの提案」

登壇者プロフィール

[株式会社日本経済新聞社](https://hack.nikkei.com/)で機械学習や自然言語処理技術を活用したサービス開発・業務支援に従事しています。論文・書籍などの執筆にも精力的に取り組んでおり、2021 年には「[The 5th IEEE Workshop on Human-in-the-Loop Methods and Future of Work in BigData](https://humanmachinedata.org/)」に論文が採択されました。

---

# 鈴木健史 @tkc79

- `20:35-21:00`: 発表
- `21:00-21:05`: 質疑応答

登壇テーマ

「Auto Labelling と Active Learning でアノテーション作業の効率が爆上がりした話」

登壇者プロフィール

早稲田大学大学院創造理工研究科修了。在学中、機械学習のアルゴリズムの研究。ワークスアプリケーションズにて、会計 SaaS 立ち上げや複数の AI プロジェクトを経験後。 その後、AI 開発におけるアノテーションの課題を解決したい思いから FastLabel を創業。 FastLabel では、アノテーションプラットフォームを開発・提供している。

---

# 杉山 阿聖 (@K_Ryuichirou)

- `21:05-21:30`: 発表
- `21:30-21:35`: 質疑応答

登壇テーマ

「NeurIPS Data-Centric AI Workshop から見る Data-Centric アプローチの現在と未来」

登壇者プロフィール

Citadel AI で Software Engineer として自社サービス開発や MLOps の啓蒙活動に従事。「見て試してわかる機械学習アルゴリズムの仕組み 機械学習図鑑」の共著者のひとり。

---

# オンライン懇親会 🎉 🕺 🎉

- `21:35-` gather で開催

アンケートで収集したメールアドレス宛にオンライン懇親会を連絡予定でしたが、入力されていない方が多数存在していました

アンケートした結果、オンライン懇親会自体当初想定した定員の 25 名よりも遥かに少ない申し込み人数なので、希望者は全員参加できると見込み、イベント参加者全員が閲覧可能な connpass の参加者への情報欄にオンライン懇親会のリンクを共有することにしました
もし、参加したかったが定員オーバーで入れない場合は、Twitter でお知らせください。追加のルームを作るなど対応します

注意) アンケートで入力されたメールアドレスでのオンライン懇親会のへの参加情報共有は今回は行いません

Connpass の `参加者への情報` に https://gather.town への招待リンクを貼っています。MLCT #13 への参加登録後に閲覧可能です
