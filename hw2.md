gantt
    title 專案甘特圖
    dateFormat  YYYY-MM-DD
    section 研擬計畫
    研擬計畫           :done,    task1, 2024-09-30, 1d
    section 任務分配
    任務分配           :done,    task2, after task1, 4d
    section 硬體相關
    取得硬體           :done,    task3, after task1, 17d
    安裝硬體           :active,  task5, after task3, 10d
    section 軟體開發
    程式開發           :active,  task4, after task2, 70d
    section 測試相關
    程式測試           :active,  task6, after task4, 30d
    系統測試           :active,  task9, after task6, 25d
    section 文件相關
    撰寫使用手冊       :active,  task7, after task5, 25d
    section 檔案相關
    轉換檔案           :active,  task8, after task5, 20d
    section 使用者相關
    使用者訓練         :active,  task10, after task7, 20d
    使用者測試         :active,  task11, after task9, 25d

