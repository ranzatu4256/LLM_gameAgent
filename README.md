# LLM_gameAgent

## 概要
このプロジェクトは、9x9のボード上で行われる戦略的なチェスバトルゲームです。プレイヤーは異なる能力を持つ4種類の駒を操り、敵チームとの戦いを繰り広げます。

## ゲームの特徴
- 9x9のカスタムチェスボード
- 4種類のユニーク駒：偵察兵、衛生兵、重装備兵、通信兵
- ターン制の戦略的バトルシステム
- 駒ごとの特殊能力
- 情報共有システム
- 衛生兵による味方の蘇生機能

## 駒の種類と能力

1. 偵察兵 (Scout)
   - 移動可能距離 : 3マス
   - 探知距離 : 4マス
   - 攻撃距離 : 3マス
   - 攻撃力：1
   - 通信可能距離 : 3マス

2. 衛生兵 (Medic)
   - 移動可能距離 : 2マス
   - 探知距離 : 3マス
   - 攻撃距離 : 3マス
   - 攻撃力：1
   - 通信可能距離 : 3マス
   - 特殊能力：倒された味方を蘇生
   - 蘇生可能距離 : 3マス

3. 重装備兵 (Heavy Infantry)
   - 移動可能距離 : 1マス
   - 探知距離 : 3マス
   - 攻撃距離 : 4マス
   - 攻撃力：3
   - 通信可能距離 : 3マス
   - 特殊能力：広範囲の攻撃が可能
   - 攻撃範囲 : 周囲1マス

4. 通信兵 (Communicator)
   - 移動可能距離 : 2マス
   - 探知距離 : 3マス
   - 攻撃距離 : 3マス
   - 攻撃力：1
   - 通信可能距離 : 4マス

## ゲームの流れ
1. 自軍の駒の移動
2. 敵軍の駒の移動
3. 情報共有
4. 自軍の攻撃対象選択
5. 敵軍の攻撃対象選択
6. ダメージ計算
7. 蘇生フェーズ
8. ターン終了

## 勝利条件
以下のいずれかの条件を満たすと勝利となります：
1. 敵の全滅
2. 自軍の駒が敵陣の一番奥のマスに到達
3. 10ターン終了時に残りのHPの合計が大きい方

## ポリシー設定のヒント
移動の選択肢には以下の情報が含まれます:
  - 移動可能なマスの相対座標
    
攻撃対象の選択肢には以下の情報が含まれます:
  - 攻撃可能な敵の相対座標
  - 攻撃可能な敵の兵科
