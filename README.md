# 上海证券交易所大宗交易 ETF 数据爬虫  

### 功能  
- 抓取上海证券交易所大宗交易历史数据。  
- 按日期范围筛选数据。  
- 提取包含 "ETF" 的证券数据行。  
- 数据保存为 CSV 文件：  
  - `all_data.csv`: 包含所有抓取数据。  
  - `etf_data.csv`: 包含仅与 ETF 相关的数据。  

### 安装步骤  
1. 安装 **Python 3.7+**。  
2. 下载 [Edge WebDriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/) 并配置路径。  
3. 安装依赖库：  
   ```bash  
   pip install selenium pandas  
   ```  

### 使用方法  
1. 修改代码中 WebDriver 路径：  
   ```python  
   service = webdriver.edge.service.Service("C:/msedgedriver.exe")  
   ```  
2. 运行脚本：  
   ```bash  
   python fetch_etf_data.py  
   ```  
3. 数据输出：  
   - `all_data.csv`: 所有交易数据。  
   - `etf_data.csv`: ETF 相关交易数据。  

### 注意事项  
- 日期范围通过 JavaScript 注入并需手动确认。  
- 脚本支持分页抓取，检测到最后一页时自动停止。  
- 需要 Edge 浏览器及对应的 WebDriver。  

---

# SSE Block Trade ETF Data Scraper  

### Features  
- Scrapes historical block trade data from the SSE website.  
- Filters data by a specified date range.  
- Extracts rows containing "ETF" in the security name.  
- Saves data to CSV files:  
  - `all_data.csv`: Contains all fetched data.  
  - `etf_data.csv`: Contains only ETF-related data.  

### Installation  
1. Install **Python 3.7+**.  
2. Download [Edge WebDriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/) and configure its path.  
3. Install dependencies:  
   ```bash  
   pip install selenium pandas  
   ```  

### Usage  
1. Update the WebDriver path in the script:  
   ```python  
   service = webdriver.edge.service.Service("C:/msedgedriver.exe")  
   ```  
2. Run the script:  
   ```bash  
   python fetch_etf_data.py  
   ```  
3. Output:  
   - `all_data.csv`: All block trade data.  
   - `etf_data.csv`: ETF-related block trade data.  

### Notes  
- Date range is injected using JavaScript and requires manual confirmation.  
- The script supports pagination and stops automatically at the last page.  
- Requires Edge browser and its corresponding WebDriver.  
