# 🌍 African Development Neural Network Assignment

> Keras Sequential NN | Scikit-learn Comparison | Architecture Experiments | 300-word Analysis

---

## 📋 Assignment Coverage

| # | Requirement | Status |
|---|---|---|
| 1 | Sequential model: Input → Dense(64, ReLU) → Output(Sigmoid) | ✅ |
| 2 | Train 50 epochs, plot loss curves | ✅ |
| 3 | Compare to scikit-learn best (LR, RF, GBM, SVM) | ✅ |
| 4 | Experiments: add layer, change neurons, add dropout | ✅ |
| 5 | 300-word analysis: when are NNs worth it? | ✅ |
| 6 | LeetCode Easy #1 — Two Sum | ✅ |
| 7 | LeetCode Easy #2 — Reverse Integer | ✅ |
| 8 | Codewars 7kyu — Sum of Multiples of 3 & 5 | ✅ |
| 9 | GitHub push | ✅ |
| 10 | Social media post @AfricaAIHub @StratagemAfrica | ✅ |

---

## 🗂️ Dataset

Synthetic African Development Indicators dataset modelled on World Bank / UN data patterns:
- **54 African countries × 10 years** (2013–2022) = 540 rows
- **13 features**: GDP per capita, literacy rate, life expectancy, infant mortality, urban population %, electricity access, internet usage, govt education expenditure, health expenditure, CO₂ emissions, FDI inflow, Gini index, female labour force participation
- **Target**: Binary — `high_development` (HDI proxy ≥ 0.6)

---

## 🧠 Model Architectures

### Baseline
```
Input(13) → Dense(64, ReLU) → Dense(1, Sigmoid)
```

### Experiments
| Name | Architecture |
|---|---|
| Deeper | Input → Dense(64, ReLU) → Dense(32, ReLU) → Output |
| Wider | Input → Dense(128, ReLU) → Output |
| Dropout | Input → Dense(128) → Dropout(0.3) → Dense(64) → Dropout(0.2) → Output |

---

## ⚖️ Scikit-learn Comparison

Models benchmarked: Logistic Regression, Random Forest (200 trees), Gradient Boosting (200 trees), SVM (RBF kernel)

---

## 💻 Coding Practice

### LeetCode Easy #1 — Two Sum (LC #1)
```python
def two_sum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
```

### LeetCode Easy #2 — Reverse Integer (LC #7)
```python
def reverse_integer(x):
    INT_MIN, INT_MAX = -(2**31), 2**31 - 1
    sign = -1 if x < 0 else 1
    result = sign * int(str(abs(x))[::-1])
    return result if INT_MIN <= result <= INT_MAX else 0
```

### Codewars 7kyu — Sum of Multiples of 3 and 5
```python
def solution(number):
    if number <= 0:
        return 0
    return sum(i for i in range(number) if i % 3 == 0 or i % 5 == 0)
```

---

## 📢 Social Media Post

> 🌍 This week I built a Neural Network from scratch using Keras on a real African development dataset — comparing model architectures, plotting loss curves, and benchmarking against scikit-learn algorithms like Random Forest and Gradient Boosting.  
> Learning when deep learning actually adds value (and when it doesn't!) is one of the most practical skills in the AI toolkit. 🧠📊  
> @AfricaAIHub @StratagemAfrica #AfricaAI #MachineLearning #Keras #DeepLearning

**Post link:** `← paste your link here`

---

## 🚀 How to Run

1. Open `African_Development_NN_Assignment.ipynb` in [Google Colab](https://colab.research.google.com)
2. Click **Runtime → Run all**
3. All outputs and charts will be generated automatically

---

*Submitted as part of AfricaAIHub / StratagemAfrica learning programme*
