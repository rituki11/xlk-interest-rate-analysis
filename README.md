# 📈 金利とXLKの関係分析プロジェクト
### Federal Funds Rate vs Technology ETF (XLK) Analysis
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rituki11/xlk-interest-rate-analysis/blob/main/analysis.ipynb)

## 🚀 プロジェクト概要
このプロジェクトでは、**FRBの政策金利（Federal Funds Rate）とテクノロジーETF（XLK）の関係を分析** しました。  
一般的に、「金利が上がると株価が下がる」と言われますが、**本当にそうなのか？ 特にハイテク株はどう影響を受けるのか？** をデータで検証しました。

## 📊 分析内容
- **FRBの金利データをFRED APIから取得し、XLKの価格データと比較**
- **短期・長期の相関関係を分析**
- **過去20年以上のデータを用いて、金利とXLKの関係の変化を可視化**
- **最新の金利動向（2024年時点）を確認し、今後のXLKの動向を考察**

## 🛠️ 使用技術
- **Python**
  - Pandas（データ処理）
  - Matplotlib / Seaborn（データ可視化）
  - yfinance（株価データ取得）
  - requests（FRED APIから金利データ取得）
- **データソース**
  - FRBの政策金利データ（FRED API）
  - テクノロジーETF（XLK）の価格データ（yfinance）

## 📈 分析結果
- **長期的には金利とXLKの相関は弱い（相関係数 0.22）**
- **2010年代後半には相関が強まる（+0.6 以上の時期あり）**
- **2022年以降、金利上昇でもXLKが上昇（AIブームなどの影響）**
- **最新の金利データ（2024年時点）では金利は下落傾向 → XLKには追い風？**

## 📂 ファイル構成
📂 analysis.ipynb - 分析コード（Google Colabで実行可能） 📂 README.md - プロジェクトの概要説明 📂 images/ - 生成したグラフ 📂 requirements.txt - 必要なライブラリ

markdown
コピーする
編集する


## 🚀 実行方法
1. 必要なライブラリをインストール
pip install -r requirements.txt

2. `analysis.ipynb` を開いて実行！

---

## **📌 参考**
- FRBの金利データ: [FRED API](https://fred.stlouisfed.org/)
- 株価データ: [Yahoo Finance](https://finance.yahoo.com/)

---


---

🚀 **このREADME.mdを追加すれば、GitHubリポジトリがより完成度の高いポートフォリオになる！**  
👉 **GitHubの「Add file」→「Create new file」→ `README.md` を作成し、上記の内容をコピペしよう！**  
👉 **終わったら、インターン応募に使える！🎯** 🚀

