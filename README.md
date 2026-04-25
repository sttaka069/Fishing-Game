FishingSystem
Unity 向けスタンドアローン釣りミニゲームコンポーネント

概要
スペースキー 1 つで遊べる釣りミニゲームシステムです。
FishingSystem.cs をアタッチするだけで既存プロジェクトにすぐ組み込めます。

セットアップ
#手順1FishingSystem.cs をプレイヤーオブジェクトにアタッチ
2水辺オブジェクトのコライダーに Water タグを設定
3コライダーの Is Trigger を ON にする
4インスペクターでパラメータを調整して完了

操作方法
状態キーアクション待機中Space釣り糸をキャスト（水辺のみ有効）ヒット中Space反応してリール開始リール中Space 連打巻き取り進捗を加速


魚図鑑
レアリティ値の逆数を重みとした加重ランダム抽選です。
rarity 1 → weight 1/1 = 1.00  (コモン)
rarity 2 → weight 1/2 = 0.50  (アンコモン)
rarity 3 → weight 1/3 = 0.33  (レア)
rarity 4 → weight 1/4 = 0.25  (エピック)
rarity 5 → weight 1/5 = 0.20  (レジェンド)

<img width="673" height="443" alt="スクリーンショット 2026-04-25 113425" src="https://github.com/user-attachments/assets/206a7c8c-f1d9-45fa-a2b0-ce5dcfb89e9a" />


インスペクター設定
csharp[Header("Settings")]
public float minWaitTime   = 2f;   // ヒットまでの最小待機時間（秒）
public float maxWaitTime   = 5f;   // ヒットまでの最大待機時間（秒）
public float biteTimeLimit = 2f;   // ヒット後の反応猶予時間（秒）
public float reelSpeed     = 0.4f; // 自動リール進捗 / 秒

ファイル構成
FishingSystem/
├── FishingSystem.cs   # メインコンポーネント
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
