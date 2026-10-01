
## Knowledge Distillation（知識蒸餾）
是一種模型壓縮技術，目的是將大型且強大的 AI 模型（Teacher Model，教師模型）的知識，轉移到較小的模型（Student Model，學生模型），讓小模型在維持接近效能的同時，擁有更快的速度、更低的記憶體需求與更少的運算成本。
```
教授（Teacher） ↓ 教學 學生（Student）
```
#### 為什麼需要 Knowledge Distillation？
大型模型通常：準確率高、推理能力強。但是：很耗 GPU、記憶體需求大、回應速度較慢、成本昂貴。<br>可能只損失一些精度，但：推論速度提升數倍、佔用記憶體大幅下降、更容易部署於邊緣設備。

#### Knowledge Distillation 流程
- Step 1：訓練大型 Teacher Model
- Step 2：Teacher 產生結果
- Step 3：Student 模仿 Teacher
- Step 4：得到小型模型

#### 與量化（Quantization）的差別
Quantization





