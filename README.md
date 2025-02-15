# quarto 發布至 github pages
 
### 第一次發布步驟：
1. 首先在 quarto 專案的 _quarto.yml 中設定輸出目錄為 docs：
   ```yaml
   project:
     type: website
     output-dir: docs
   ```

2. 在根目錄新增 .nojekyll 檔案

3. 在終端機執行以下指令，將網站渲染至 docs 目錄：
   ```bash
   quarto render
   ```

4. 將變更提交至 GitHub(只提交 docs 目錄)：
   ```bash
   git add docs
   git commit -m "Publish site to docs/" (提交訊息自訂)
   git push
   ```

4. 在 GitHub repository 設定中：
   - 前往 Settings > Pages
   - 在 Build and deployment 區段
   - Source 選擇 "Deploy from a branch"
   - Branch 選擇 "main" 和 "/docs"
   - 儲存設定

完成以上步驟後，您的網站將會發布在 `https://<username>.github.io/<repository>/`

### 維護步驟：
1. 在終端機執行以下指令，將網站渲染至 docs 目錄：
   ```bash
   quarto render
   ```

2. 將變更提交至 GitHub (只提交 docs 目錄 or 所有變更)
