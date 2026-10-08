
Week5-EAI_lec3_pruning

## 知識點：
### Network Pruning（網路剪枝）
Network Pruning（網路剪枝）是一種模型壓縮技術，主要目的在於移除神經網絡中不重要或冗餘的權重（Weights）、神經元或結構，藉此減少模型參數量、降低計算複雜度與記憶體佔用，並在盡可能維持模型準確度的前提下，提升推論（Inference）效率。
- 根據剪枝的粒度與結構，主要可分為以下三種方式：
  - 非結構化剪枝（Unstructured Pruning）：直接移除數值較小的權重（Remove weights with small magnitude）。此方法通常能維持較高的模型準確度，但會產生稀疏矩陣（Sparse Matrix），若缺少特殊硬體支援較難直接加速。
  - 結構化剪枝（Structured Pruning）：直接移除整列、整欄或整個通道（Remove entire rows/columns/channels）。這種方式對硬體極為友善（Hardware-friendly），方便解碼與平行計算，能直接顯著提升推論速度。
  - 半結構化剪枝（Semi-structured Pruning）：將矩陣切分為小區塊（Blocks），並移除部分區塊或在每個區塊內移除固定數量的權重。其目標是在非結構化與結構化剪枝之間取得更好的權衡（Trade-offs）。
- 通常在完成剪枝後，會透過微調（Fine-tuning）再次訓練網路，以補償因移除權重而損失的準確度。






Network Pruning（網路剪枝） 是深度學習中一種**模型壓縮（Model Compression）**技術，目的是將神經網路中「不重要」的神經元、權重或通道移除，讓模型變得更小、更快，同時盡量維持原本的準確率。
- 為什麼需要 Network Pruning？
  <br>現代神經網路通常有大量參數，例如：AlexNet：約 6000 萬參數、VGG16：約 1.38 億參數、LLM（大型語言模型）：數十億至數千億參數。然而研究發現：許多權重對最終結果影響很小，即使刪除也不會明顯降低模型效能。因此可以透過 Pruning 將模型「瘦身」。
- 


























