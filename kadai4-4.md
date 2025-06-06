## 自動販売機（オブジェクト、DOM、イベント処理）のミニレポート
### Q4-1. Itemクラスのメソッドについて説明せよ。
* showItemListがクラスメソッドである理由を考察せよ。
 　このメソッドが特定される商品のインスタンスに依存しない処理を行い、商品全体を表示
 するように設計され、クラスメソッドにした。　
* buyItemがインスタンスメソッドである理由を考察せよ。
　　buyItemが特定される商品のオブジェクトの状態の変更を伴うである。購入処理により、特定される
　商品の数を減らす処理をしなければならない、よって個別のオブジェクトのプロパティを変更する操作
　であるため、インスタンスメソッドにした。
### Q4-2. 商品の購入ボタンをクリックすると、どのような処理でセルの値が減少するか説明せよ。
* 購入された商品の在庫数のセルをどのようにして特定するのか説明せよ。
　　商品の在庫数を表示するセルはidを利用して行われる。表を作成する時、各商品の在庫数セルには"stock" + 商品IDという形
　式でid属性が設定される。buyItemメソッド内では、document.getElementById("stock" + this.id)を使用して、購入された商品に対応する在庫数セルを　特定できる。
* 特定したセルの値をどのように変更するのか説明せよ。
　　特定されたHTML要素の内容変更は、textContentプロパティを使用して行われている。if文で要素があるか判断し、要素が正常に入手できた場合のみ処理を行われる。要素の更新は、stockElement.textContent = this.stockという文を代入により実現された。
### Q4-3. 感想
* 今回の課題で苦労したこと
　　HTML要素の動的な生成とDOM操作の連携に対し、最初は処理の流れをはあくするのに苦労した。
* 演習を通して理解できたこと
　　オブジェクト指向プログラミングの基本概念について実践的な理解を得ることができた。特に、クラスとインスタンスの違い、staticメソッドとインスタン　スメソッドの使い分けについて、実際のコード実装を通じて学習できた。
* この自動販売機プログラムの追加機能や課題など
　　購入履歴とか商品の画像とかカテゴリーとかユーザの体験の向上を助ける機能が不足している。
