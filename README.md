程式解釋：
AdaptivePID 類別：
這個類別定義了PID控制器的核心邏輯，包括：

update() 方法：根據當前的溫度和目標設定點計算控制輸出。

adapt() 方法：根據控制效果（如誤差和控制努力）動態調整PID參數。

仿真循環：
程式通過一個循環模擬溫度隨時間的變化，每次迭代更新PID控制器的輸出，並根據控制輸出來調整溫度。
溫度會隨時間改變，PID控制器會根據反饋自動調整其參數。

自適應PID參數調整：
控制器會根據系統的表現進行自適應調整，例如：

當誤差較大時，增大比例增益（Kp）。
當控制努力過大時，減小積分增益（Ki）。
當誤差較小時，增大微分增益（Kd）以更精確地控制系統。
仿真結果輸出：
程式會在仿真結束後輸出一些關鍵性能指標，如最終溫度、誤差、穩定時間（±0.5°C的範圍內），最大過衝（溫度的最大偏離設定點的數值），以及最終調整過的PID參數。

繪圖：
程式會繪製溫度隨時間變化的圖表，並標示出設定點，讓您能夠直觀地查看控制系統的響應。
