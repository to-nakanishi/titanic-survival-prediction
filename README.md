Titanic Survival Prediction(Kaggle提供：https://www.kaggle.com/)  
　タイタニック号の乗客生存予測モデルを構築  

1.結果  
　・Kaggleスコア: 77.7% (上位33%)  
　・モデル: RandomForest  
　・主要特徴量: Sex, Pclass, Age, Fare, Has_Cabin  

2.特徴  
　Cabin処理（特徴量工夫の事例）   
　Cabinの欠損率が77%と高いため、以下を想定。  
  仮説：「客室記載=上位クラスのゲスト」と考え、生存率を比較。  
　Cabin情報あり：67% 生存率  
　情報なし：30% 生存率  
  → 有意な差があるため、削除ではなくHas_Cabinフラグを作成し、モデルに組み込み  

3.技術  
 Python, pandas, matplotlib、 scikit-learn　RandomForest  

4.ファイル  
　・train.csv, test.csv: Kaggleサイト参照  
　・titanic.ipynb: 分析ノートブック  
　・submission.csv: 提出結果  

5.学び  
　・カテゴリ変数の効率的な処理  
　・ビジネス仮説に基づくEDA  
　・RandomForestの実装と評価  
