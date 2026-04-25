FishingSystem
Unity 向けスタンドアローン釣りミニゲームコンポーネント

概要
スペースキー 1 つで遊べる釣りミニゲームシステムです。
FishingSystem.cs をアタッチするだけで既存プロジェクトにすぐ組み込めます。

セットアップ
#手順1FishingSystem.cs をプレイヤーオブジェクトにアタッチ2水辺オブジェクトのコライダーに Water タグを設定3コライダーの Is Trigger を ON にする4インスペクターでパラメータを調整して完了

操作方法
状態キーアクション待機中Space釣り糸をキャスト（水辺のみ有効）ヒット中Space反応してリール開始リール中Space 連打巻き取り進捗を加速

状態遷移
#mermaid-rj8{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-rj8 .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-rj8 .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-rj8 .error-icon{fill:#CC785C;}#mermaid-rj8 .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-rj8 .edge-thickness-normal{stroke-width:1px;}#mermaid-rj8 .edge-thickness-thick{stroke-width:3.5px;}#mermaid-rj8 .edge-pattern-solid{stroke-dasharray:0;}#mermaid-rj8 .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-rj8 .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-rj8 .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-rj8 .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rj8 .marker.cross{stroke:#A1A1A1;}#mermaid-rj8 svg{font-family:inherit;font-size:16px;}#mermaid-rj8 p{margin:0;}#mermaid-rj8 defs #statediagram-barbEnd{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rj8 g.stateGroup text{fill:#A1A1A1;stroke:none;font-size:10px;}#mermaid-rj8 g.stateGroup text{fill:#E5E5E5;stroke:none;font-size:10px;}#mermaid-rj8 g.stateGroup .state-title{font-weight:bolder;fill:#E5E5E5;}#mermaid-rj8 g.stateGroup rect{fill:transparent;stroke:#A1A1A1;}#mermaid-rj8 g.stateGroup line{stroke:#A1A1A1;stroke-width:1;}#mermaid-rj8 .transition{stroke:#A1A1A1;stroke-width:1;fill:none;}#mermaid-rj8 .stateGroup .composit{fill:#f4f4f4;border-bottom:1px;}#mermaid-rj8 .stateGroup .alt-composit{fill:#e0e0e0;border-bottom:1px;}#mermaid-rj8 .state-note{stroke:#A1A1A1;fill:#2D2D2D;}#mermaid-rj8 .state-note text{fill:#E5E5E5;stroke:none;font-size:10px;}#mermaid-rj8 .stateLabel .box{stroke:none;stroke-width:0;fill:transparent;opacity:0.5;}#mermaid-rj8 .edgeLabel .label rect{fill:transparent;opacity:0.5;}#mermaid-rj8 .edgeLabel{background-color:transparent;text-align:center;}#mermaid-rj8 .edgeLabel p{background-color:transparent;}#mermaid-rj8 .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rj8 .edgeLabel .label text{fill:#E5E5E5;}#mermaid-rj8 .label div .edgeLabel{color:#E5E5E5;}#mermaid-rj8 .stateLabel text{fill:#E5E5E5;font-size:10px;font-weight:bold;}#mermaid-rj8 .node circle.state-start{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rj8 .node .fork-join{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rj8 .node circle.state-end{fill:#A1A1A1;stroke:#f4f4f4;stroke-width:1.5;}#mermaid-rj8 .end-state-inner{fill:#f4f4f4;stroke-width:1.5;}#mermaid-rj8 .node rect{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rj8 .node polygon{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rj8 #statediagram-barbEnd{fill:#A1A1A1;}#mermaid-rj8 .statediagram-cluster rect{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rj8 .cluster-label,#mermaid-rj8 .nodeLabel{color:#E5E5E5;}#mermaid-rj8 .statediagram-cluster rect.outer{rx:5px;ry:5px;}#mermaid-rj8 .statediagram-state .divider{stroke:#A1A1A1;}#mermaid-rj8 .statediagram-state .title-state{rx:5px;ry:5px;}#mermaid-rj8 .statediagram-cluster.statediagram-cluster .inner{fill:#f4f4f4;}#mermaid-rj8 .statediagram-cluster.statediagram-cluster-alt .inner{fill:#CC785C;}#mermaid-rj8 .statediagram-cluster .inner{rx:0;ry:0;}#mermaid-rj8 .statediagram-state rect.basic{rx:5px;ry:5px;}#mermaid-rj8 .statediagram-state rect.divider{stroke-dasharray:10,10;fill:#CC785C;}#mermaid-rj8 .note-edge{stroke-dasharray:5;}#mermaid-rj8 .statediagram-note rect{fill:#2D2D2D;stroke:#A1A1A1;stroke-width:1px;rx:0;ry:0;}#mermaid-rj8 .statediagram-note rect{fill:#2D2D2D;stroke:#A1A1A1;stroke-width:1px;rx:0;ry:0;}#mermaid-rj8 .statediagram-note text{fill:#E5E5E5;}#mermaid-rj8 .statediagram-note .nodeLabel{color:#E5E5E5;}#mermaid-rj8 .statediagram .edgeLabel{color:red;}#mermaid-rj8 #dependencyStart,#mermaid-rj8 #dependencyEnd{fill:#A1A1A1;stroke:#A1A1A1;stroke-width:1;}#mermaid-rj8 .statediagramTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-rj8 :root{--mermaid-font-family:inherit;}Space（水辺のみ）タイマー満了（2〜5秒）Space（2秒以内）タイムアウト／失敗進捗 100%／成功IdleWaitingBiteReeling

魚図鑑
レアリティ値の逆数を重みとした加重ランダム抽選です。
rarity 1 → weight 1/1 = 1.00  (コモン)
rarity 2 → weight 1/2 = 0.50  (アンコモン)
rarity 3 → weight 1/3 = 0.33  (レア)
rarity 4 → weight 1/4 = 0.25  (エピック)
rarity 5 → weight 1/5 = 0.20  (レジェンド)
魚名rarity出現率（目安）サイズ範囲Anchovy1約 26%0.5〜2 cmBream1約 26%2〜5 cmLargemouth Bass1約 26%4〜8 cmRed Snapper1約 26%15〜20 cmTrout1約 26%5〜10 cmCarp1約 26%1〜2 cmGoldfish2約 13%0.5〜1 cmYellowfin Tuna3約 9%30〜50 cmEel4約 7%2〜3 cmWhiptail Catfish5約 5%3〜4 cm

インスペクター設定
csharp[Header("Settings")]
public float minWaitTime   = 2f;   // ヒットまでの最小待機時間（秒）
public float maxWaitTime   = 5f;   // ヒットまでの最大待機時間（秒）
public float biteTimeLimit = 2f;   // ヒット後の反応猶予時間（秒）
public float reelSpeed     = 0.4f; // 自動リール進捗 / 秒

ファイル構成
FishingSystem/
├── FishingSystem.cs   # メインコンポーネント（これだけでOK）
└── README.md

技術仕様

エンジン : Unity 2020.3 以上推奨
言語 : C#
外部依存 : なし（UnityEngine のみ）
入力 : Input.GetKeyDown（旧入力システム）
水辺判定 : OnTriggerEnter / OnTriggerExit（タグ: Water）


今後の拡張候補

 釣具システム — 竿・仕掛けの種類でレア度補正・リール速度を変化
 時間帯・天候 — 時刻や天候で出現魚を変化
 図鑑 UI — 釣った魚を記録するコレクション画面
 リールミニゲーム — リール中にゲージを操作する反射ゲーム
 ScriptableObject 対応 — 魚データをアセット管理してデザイナーが編集可能に
 新入力システム対応 — Input System パッケージへの移行
