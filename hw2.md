# 工作分解結構清單

| 任務 | 說明         | 需時（天） | 前置任務 |
| ---- | ------------ | ---------- | -------- |
| 1    | 研擬計畫     | 1          | -        |
| 2    | 任務分配     | 4          | 1        |
| 3    | 取得硬體     | 17         | 1        |
| 4    | 程式開發     | 70         | 2        |
| 5    | 安裝硬體     | 10         | 3        |
| 6    | 程式測試     | 30         | 4        |
| 7    | 撰寫使用手冊 | 25         | 5        |
| 8    | 轉換檔案     | 20         | 5        |
| 9    | 系統測試     | 25         | 6        |
| 10   | 使用者訓練   | 20         | 7, 8     |
| 11   | 使用者測試   | 25         | 9, 10    |

# PERT/CPM 圖

```mermaid
graph TD
    A[研擬計畫 1天] --> B[任務分配 4天]
    A --> C[取得硬體 17天]
    B --> D[程式開發 70天]
    C --> E[安裝硬體 10天]
    D --> F[程式測試 30天]
    E --> G[撰寫使用手冊 25天]
    E --> H[轉換檔案 20天]
    F --> I[系統測試 25天]
    G --> J[使用者訓練 20天]
    H --> J
    I --> K[使用者測試 25天]
    J --> K

``````
# 甘特圖
```mermaid
gantt
    title 專案甘特圖
    dateFormat  YYYY-MM-DD
    section 研擬及取得資源
    研擬計畫            :done,  task1, 2024-10-01, 1d
    任務分配            :active, task2, after task1, 4d
    取得硬體            :active, task3, after task1, 17d
    section 程式開發及測試
    程式開發            :        task4, after task2, 70d
    程式測試            :        task6, after task4, 30d
    section 安裝及系統整合
    安裝硬體            :        task5, after task3, 10d
    撰寫使用手冊        :        task7, after task5, 25d
    轉換檔案            :        task8, after task5, 20d
    section 系統測試及驗收
    系統測試            :        task9, after task6, 25d
    使用者訓練          :        task10, after task7, 20d
    使用者訓練          :        task10, after task8, 20d
    使用者測試          :        task11, after task9, 25d
    使用者測試          :        task11, after task10, 25d
``````
# 關鍵路徑
```mermaid
graph TD
    A[研擬計畫 1天] --> B[任務分配 4天]
    B --> D[程式開發 70天]
    D --> F[程式測試 30天]
    F --> I[系統測試 25天]
    I --> K[使用者測試 25天]
``````
