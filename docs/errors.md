# 🚀 エラー対策 & デバッグログ
このドキュメントでは、`xlk-interest-rate-analysis` で発生したエラーとその解決策をまとめます。

---

## 🔥 **【KeyError】カラムが見つからないエラー**
**エラー内容:**
KeyError: '^N225_return'

**原因:**  
- カラム名が `^N225_return` になっていない  
- データ取得時にカラム名が変わっている可能性あり  

**解決策:**
```python
 すべてのカラムを確認
print("カラム一覧:", df.columns.tolist())

# カラム名を統一
df = df.rename(columns={"^N225_return": "nikkei_return"})

NameError: name 'df' is not defined
原因:

df が正しく作成されていない
run_prediction_pipeline() を実行する前に df を定義していない
解決策:

python
コピーする
編集する
if 'df' not in locals():
    print("エラー: df が未定義です！データ取得パイプラインを実行してください。")

XGBoostError: Feature names mismatch
原因:

訓練データとテストデータでカラム名が違う
前処理のどこかでデータの形が崩れている
解決策:

python
コピーする
編集する
# カラムの整合性を確認
print("X_train:", X_train.columns.tolist())
print("X_test:", X_test.columns.tolist())

# カラムが異なる場合、一致させる
X_test = X_test[X_train.columns]



5️⃣ **「Commit new file」をクリックして保存！**

---

### **✅ 方法 2: 新しいリポジトリを作る (`error-handling-guide`)**
👉 **今後、他のプロジェクトでも共通のエラー対策を使いたいなら、新しいリポジトリを作るのもアリ！**

### **📌 手順**
1️⃣ **GitHubのトップページで「New repository」をクリック**  
2️⃣ **リポジトリ名:** `error-handling-guide`  
3️⃣ **README.md を追加する**  
4️⃣ **「Create repository」ボタンをクリック**  
5️⃣ **`docs/errors.md` を作成し、すべてのプロジェクトのエラー対策をまとめる**  

📌 **新しいリポジトリの `README.md` 例**
```markdown
# 🔥 Pythonエラー対策ガイド
このリポジトリでは、データ分析・機械学習のエラーと解決策をまとめています。

## 📌 エラー一覧
- [エラー対策 & デバッグログ (`errors.md`)](docs/errors.md)

## 📂 プロジェクトでの使い方
各プロジェクトで共通のエラー対策を適用する場合、このリポジトリを参考にしてください。
