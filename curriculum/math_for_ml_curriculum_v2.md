# Math for ML - Complete Learning Path (v2)

## Curriculum Philosophy

> **"Learn math through the lens of ML problems, not abstract concepts first."**

Each topic answers: **"What ML problem does this solve?"**

---

## Your Progress Tracker

**Overall Completion: 25% (5/20 topics)**

**Estimated Timeline: 40 weeks (10 months) at 2-3 hours/week**

---

## Visual Dependency Map

```
LAYER 1: FOUNDATION (Complete ✅)
├─ 1. Vectors ✅ ─────────────────┐
├─ 2. Euclidean Distance ✅ ──────┤
├─ 3. Dot Product ✅ ─────────────┤
├─ 4. Single Neuron ✅ ───────────┤
└─ 5. Gradient Descent ✅ ────────┘
                                  │
                                  ↓
LAYER 2: SCALING (Next)
├─ 6. Matrices ⏳ ← YOU ARE HERE
├─ 7. Matrix Multiplication ⏳
└─ 8. Backpropagation ⏳
                                  │
                                  ↓
LAYER 3: CALCULUS
├─ 9. Derivatives & Partial Derivatives ⏳
├─ 10. Chain Rule ⏳
└─ 11. Activation Functions ⏳
                                  │
                                  ↓
LAYER 4: TRAINING
├─ 12. Loss Functions ⏳
├─ 13. Optimization Algorithms ⏳
└─ 14. Regularization ⏳
                                  │
                                  ↓
LAYER 5: UNCERTAINTY
└─ 15. Probability & Statistics ⏳
                                  │
                                  ↓
LAYER 6: DATA PATTERNS (New)
├─ 16. Covariance & Correlation ⏳
├─ 17. Eigenvalues & Eigenvectors ⏳
├─ 18. PCA ⏳
└─ 19. SVD & Matrix Factorization ⏳
                                  │
                                  ↓
LAYER 7: DEBUGGING
└─ 20. Gradient Flow Problems ⏳
```

**Legend:**
- ✅ Completed
- ⏳ Not Started

---

## ML Problems Covered

| Category | Problems | Coverage |
|----------|----------|----------|
| Making Predictions | 5/5 | 100% |
| Learning from Data | 6/6 | 100% |
| Handling Complex Data | 5/5 | 100% |
| Understanding Uncertainty | 5/6 | 83% |
| Non-Linear Learning | 4/4 | 100% |
| Debugging Training | 2/4 | 50% |
| **TOTAL** | **27/30** | **90%** |

---

# LAYER 1: FOUNDATION

---

## TOPIC 1: Vectors ✅

### ML Problem It Solves
> "How does a computer understand a song, an image, or a person?"

### The Answer
Everything becomes a **list of numbers** (vector).

### Real ML Examples
| Real Thing | Vector Representation |
|------------|----------------------|
| Song | [tempo, energy, danceability, ...] |
| Image pixel | [red, green, blue] |
| User preference | [action=0.8, comedy=0.3, drama=0.5] |
| Word | [0.2, -0.5, 0.8, ...] (300 numbers) |

### What You Can Do After This Topic
- ✅ Understand why ML needs vectors
- ✅ Convert real things to vectors conceptually
- ✅ Read vector notation: **x** = [x₁, x₂, x₃]

### Status: COMPLETED

---

## TOPIC 2: Euclidean Distance ✅

### ML Problem It Solves
> "How does Spotify know which songs are similar to the one I like?"

### The Answer
Measure **distance** between vectors. Small distance = similar.

### Formula
```
distance = √[(x₁-y₁)² + (x₂-y₂)² + ...]
```

### Real ML Examples
| Application | What Distance Measures |
|-------------|----------------------|
| Recommendations | How similar are two users/items? |
| K-Nearest Neighbors | Which training examples are closest? |
| Clustering | Which cluster center is nearest? |
| Anomaly detection | How far from normal? |

### What You Can Do After This Topic
- ✅ Calculate distance between two vectors
- ✅ Understand "similarity" in ML terms
- ✅ Know when to use distance (finding similar things)

### Status: COMPLETED

---

## TOPIC 3: Dot Product ✅

### ML Problem It Solves
> "How does a neuron combine all its inputs to make a decision?"

### The Answer
**Dot product** = multiply pairs, sum results.

### Formula
```
a · b = a₁b₁ + a₂b₂ + a₃b₃ + ...
```

### Real ML Examples
| Application | What Dot Product Does |
|-------------|----------------------|
| Neuron computation | Combines inputs with weights |
| Attention mechanism | Measures relevance between words |
| Similarity (cosine) | How aligned are two vectors? |

### Key Insight
- **High positive** = vectors point same direction (similar)
- **Near zero** = vectors are perpendicular (unrelated)
- **Negative** = vectors point opposite (dissimilar)

### What You Can Do After This Topic
- ✅ Calculate dot product
- ✅ Understand neuron = dot product + activation
- ✅ Know difference: distance (how far) vs dot product (how aligned)

### Status: COMPLETED

---

## TOPIC 4: Single Neuron ✅

### ML Problem It Solves
> "How does ML make a prediction from data?"

### The Answer
```
prediction = inputs · weights + bias
```

### The Process
1. Data comes in (vector of inputs)
2. Each input has a weight (importance)
3. Dot product combines them
4. Add bias
5. Output prediction

### Real ML Example
```
Spam detector:
- Input: [word_count, has_link, caps_ratio] = [50, 1, 0.3]
- Weights: [0.1, 0.8, 0.5] (learned)
- Prediction: 50×0.1 + 1×0.8 + 0.3×0.5 = 5.95 → likely spam
```

### What You Can Do After This Topic
- ✅ Explain how a neuron makes predictions
- ✅ Calculate neuron output by hand
- ✅ Understand weights = what patterns to look for

### Status: COMPLETED

---

## TOPIC 5: Gradient Descent (Single Neuron) ✅

### ML Problem It Solves
> "How does ML learn the right weights?"

### The Answer
1. Make prediction
2. Calculate error (how wrong)
3. Adjust weights in direction that reduces error
4. Repeat

### The Update Rule
```
w_new = w_old + learning_rate × error × input
```

### Why This Works
- Error tells us **how much** to change
- Input tells us **which weight** to change most
- Learning rate controls **step size**

### Real ML Example
```
Prediction: 5.95 (said spam)
Actual: 0 (not spam)
Error: 0 - 5.95 = -5.95

Update weights to make prediction smaller next time.
```

### What You Can Do After This Topic
- ✅ Explain gradient descent as a learning process
- ✅ Calculate weight updates by hand
- ✅ Understand why error × input makes sense

### Status: COMPLETED

---

# LAYER 2: SCALING

---

## TOPIC 6: Matrices ⏳

### ML Problem It Solves
> "How does ML process 1000 images at once instead of one at a time?"

### The Answer
Organize data into a **matrix** (2D grid of numbers).

### Why ML Needs This
| Without Matrices | With Matrices |
|------------------|---------------|
| Process 1 image | Process 1000 images |
| 1 neuron's weights | 128 neurons' weights |
| Loop through data | Single operation |
| Slow | Fast (GPU optimized) |

### Real ML Examples
| Matrix | Rows | Columns |
|--------|------|---------|
| Batch of images | 1000 images | 784 pixels each |
| Layer weights | 128 neurons | 784 inputs each |
| Word embeddings | 50,000 words | 300 dimensions |

### Learning Objectives
- [ ] Understand matrix dimensions (rows × columns)
- [ ] Know matrix as "collection of vectors"
- [ ] Recognize when vectors become matrices in ML

### Estimated Sessions: 2

---

## TOPIC 7: Matrix Multiplication ⏳

### ML Problem It Solves
> "How does ML compute an entire layer's output in one operation?"

### The Answer
**Matrix multiplication** = many dot products at once.

### The Magic
```
# Without matrix multiply (slow)
for each input in batch:
    for each neuron:
        output = dot_product(input, weights)

# With matrix multiply (fast)
outputs = inputs @ weights  # One line!
```

### Real ML Application
```
Forward pass through one layer:
- Input: 1000 images × 784 pixels
- Weights: 784 inputs × 128 neurons
- Output: 1000 images × 128 outputs

All computed in ONE matrix multiplication!
```

### Learning Objectives
- [ ] Calculate matrix multiplication step-by-step
- [ ] Understand dimension rules (m×n @ n×p = m×p)
- [ ] See forward pass as matrix multiplication

### Estimated Sessions: 2

---

## TOPIC 8: Backpropagation ⏳

### ML Problem It Solves
> "How does a deep network with 100 layers learn? How do errors flow back?"

### The Answer
**Backpropagation** = send error backward through layers, update each layer's weights.

### Why Simple Gradient Descent Isn't Enough
| Single Neuron | Deep Network |
|---------------|--------------|
| Error directly affects weight | Error passes through many layers |
| One update | Chain of updates |
| "I was wrong by 5" | "Layer 3 was wrong because Layer 2 was wrong because..." |

### The Process
1. **Forward pass**: Input → Layer 1 → Layer 2 → ... → Output
2. **Calculate error** at output
3. **Backward pass**: Error flows back, each layer gets its "share"
4. **Update weights** at each layer

### Real ML Application
- Training GPT: gradients flow back through billions of parameters
- Training ResNet: gradients flow through 152 layers

### Learning Objectives
- [ ] Explain why backprop is needed for deep networks
- [ ] Trace gradient flow backward through layers
- [ ] Understand each layer's gradient depends on layers after it

### Estimated Sessions: 3

---

# LAYER 3: CALCULUS

---

## TOPIC 9: Derivatives & Partial Derivatives ⏳

### ML Problem It Solves
> "How do I know which direction to change weights to reduce error?"

### The Answer
**Derivative** = rate of change. Tells you the **slope**.

### Why ML Needs This
```
If slope is positive: increasing weight increases error → decrease weight
If slope is negative: increasing weight decreases error → increase weight
```

### Partial Derivatives
When you have **many weights**, you need to know:
- How does error change if I change weight₁? (∂E/∂w₁)
- How does error change if I change weight₂? (∂E/∂w₂)
- etc.

**Gradient** = vector of all partial derivatives

### Real ML Application
```
Loss = 0.5 × (prediction - actual)²

∂Loss/∂prediction = (prediction - actual)

This tells us: if prediction is too high, gradient is positive, 
so we should decrease prediction.
```

### Learning Objectives
- [ ] Understand derivative as "slope" or "rate of change"
- [ ] Calculate simple derivatives (x², 2x)
- [ ] Understand partial derivatives (change one variable, hold others fixed)
- [ ] Know gradient = direction of steepest increase

### Estimated Sessions: 2-3

---

## TOPIC 10: Chain Rule ⏳

### ML Problem It Solves
> "In a deep network, how do I find the gradient for a weight in Layer 1 when the error is at the output?"

### The Answer
**Chain rule**: Multiply the derivatives along the path.

### The Intuition
```
If A affects B, and B affects C:
How much does A affect C?

Answer: (how A affects B) × (how B affects C)
```

### Real ML Application
```
Input → Layer 1 → Layer 2 → Layer 3 → Loss

∂Loss/∂(Layer1_weights) = 
    ∂Loss/∂Layer3 × ∂Layer3/∂Layer2 × ∂Layer2/∂Layer1
```

### Why This Is Critical
- Backpropagation IS the chain rule applied repeatedly
- Without chain rule, can't train deep networks
- Explains vanishing/exploding gradients

### Learning Objectives
- [ ] Apply chain rule to nested functions
- [ ] See backprop as chain rule
- [ ] Understand gradient = product of many terms

### Estimated Sessions: 2

---

## TOPIC 11: Activation Functions ⏳

### ML Problem It Solves
> "Why can't a neural network with only linear operations learn complex patterns?"

### The Answer
Without **non-linearity**, deep network = one linear operation.

### The Problem
```
Linear(Linear(Linear(x))) = Linear(x)

100 linear layers = 1 linear layer!
```

### The Solution: Activation Functions
| Function | Formula | When to Use |
|----------|---------|-------------|
| ReLU | max(0, x) | Hidden layers (default) |
| Sigmoid | 1/(1+e⁻ˣ) | Binary output (0 to 1) |
| Softmax | eˣⁱ/Σeˣ | Multi-class output (probabilities) |
| Tanh | tanh(x) | Output between -1 and 1 |

### Real ML Application
```
Layer output = activation(inputs @ weights + bias)

Without activation: can only learn straight lines
With activation: can learn any pattern
```

### Learning Objectives
- [ ] Explain why non-linearity is required
- [ ] Know when to use each activation
- [ ] Calculate activation outputs
- [ ] Understand activation derivatives (for backprop)

### Estimated Sessions: 2

---

# LAYER 4: TRAINING

---

## TOPIC 12: Loss Functions ⏳

### ML Problem It Solves
> "How do I measure how wrong my model is? And why use different measures for different tasks?"

### The Answer
**Loss function** = measures error in a way that's useful for learning.

### Different Tasks, Different Losses
| Task | Loss Function | Why |
|------|---------------|-----|
| Predict a number | Mean Squared Error | Penalizes big errors more |
| Yes/No classification | Binary Cross-Entropy | Works with probabilities |
| Multi-class | Cross-Entropy | Compares probability distributions |

### Why Not Just Use "Percent Wrong"?
```
Percent wrong: 30% → 29% → 28%  (no gradient information!)
Cross-entropy: 0.85 → 0.73 → 0.61 (smooth, has gradient)
```

### Real ML Application
```
# Regression (predict house price)
loss = mean((predicted - actual)²)

# Classification (predict cat vs dog)
loss = -[y×log(p) + (1-y)×log(1-p)]
```

### Learning Objectives
- [ ] Know which loss for which task
- [ ] Calculate MSE and Cross-Entropy
- [ ] Understand why cross-entropy works for classification
- [ ] Calculate loss derivatives

### Estimated Sessions: 2

---

## TOPIC 13: Optimization Algorithms ⏳

### ML Problem It Solves
> "Plain gradient descent is slow. How do modern networks train faster?"

### The Answer
Better optimizers: **Momentum**, **RMSprop**, **Adam**.

### Problems with Plain Gradient Descent
| Problem | What Happens |
|---------|--------------|
| Oscillation | Zig-zags instead of going straight |
| Stuck | Gets trapped in flat regions |
| Same learning rate | Some weights need big steps, others small |

### Modern Optimizers
| Optimizer | Key Idea |
|-----------|----------|
| **Momentum** | Accumulate direction (like a ball rolling) |
| **RMSprop** | Adapt learning rate per parameter |
| **Adam** | Momentum + RMSprop (most popular) |

### Real ML Application
```python
# Almost every modern network
optimizer = Adam(learning_rate=0.001)
```

### Learning Objectives
- [ ] Understand why plain gradient descent is limited
- [ ] Explain momentum intuitively
- [ ] Know why Adam is default
- [ ] Recognize optimizers in code

### Estimated Sessions: 2

---

## TOPIC 14: Regularization ⏳

### ML Problem It Solves
> "My model is 99% accurate on training data but 60% on new data. Why?"

### The Answer
**Overfitting**. Model memorized training data instead of learning patterns.

### Regularization Techniques
| Technique | How It Works |
|-----------|--------------|
| **L2 (Weight Decay)** | Penalize large weights |
| **Dropout** | Randomly disable neurons during training |
| **Early Stopping** | Stop before overfitting |
| **Data Augmentation** | Create more training examples |

### Why Regularization Works
- Large weights = model is "trying too hard" to fit training data
- Dropout = forces redundancy, no single neuron is critical
- Early stopping = stop while model still generalizes

### Real ML Application
```python
# L2 regularization
loss = prediction_loss + 0.01 × sum(weights²)

# Dropout
layer = Dropout(0.5)  # Disable 50% of neurons randomly
```

### Learning Objectives
- [ ] Explain overfitting vs underfitting
- [ ] Know when to use which regularization
- [ ] Understand L2 mathematically
- [ ] Recognize regularization in code

### Estimated Sessions: 2

---

# LAYER 5: UNCERTAINTY

---

## TOPIC 15: Probability & Statistics ⏳

### ML Problem It Solves
> "How confident should my model be? What does 80% probability actually mean?"

### The Answer
Understand **probability distributions**, **uncertainty**, and **Bayes' theorem**.

### Core Concepts
| Concept | ML Application |
|---------|----------------|
| Probability distribution | Model outputs (softmax = distribution) |
| Mean, Variance | Data analysis, normalization |
| Gaussian distribution | Weight initialization, noise modeling |
| Bayes' theorem | Update beliefs with new evidence |

### Real ML Applications
```
Softmax output: [0.7, 0.2, 0.1]
→ 70% confident it's class A
→ But what does that mean?

Gaussian distribution:
→ Initialize weights randomly from N(0, 0.01)
→ Add noise for robustness
```

### Learning Objectives
- [ ] Understand probability distributions
- [ ] Calculate mean, variance, standard deviation
- [ ] Know Gaussian distribution (most important)
- [ ] Apply Bayes' theorem
- [ ] Interpret model confidence

### Estimated Sessions: 3

---

# LAYER 6: DATA PATTERNS (New)

---

## TOPIC 16: Covariance & Correlation ⏳

### ML Problem It Solves
> "Do these two features move together? If height increases, does weight increase?"

### The Answer
**Covariance** = do variables change together?
**Correlation** = same, but normalized to [-1, 1]

### Why ML Needs This
| Application | Why |
|-------------|-----|
| Feature selection | Remove redundant features |
| Understanding data | Which features are related? |
| PCA foundation | PCA uses covariance matrix |
| Debugging | Why is my model learning X instead of Y? |

### The Intuition
```
Covariance > 0: When X goes up, Y tends to go up
Covariance < 0: When X goes up, Y tends to go down
Covariance ≈ 0: X and Y are independent
```

### Real ML Application
```
Features: [age, income, spending]

Covariance matrix shows:
- age-income: positive (older = higher income)
- income-spending: positive (more money = more spending)
- age-spending: ??? (need to check)
```

### Learning Objectives
- [ ] Calculate covariance between two variables
- [ ] Understand covariance matrix
- [ ] Know difference: covariance vs correlation
- [ ] Apply to feature analysis

### Estimated Sessions: 2

---

## TOPIC 17: Eigenvalues & Eigenvectors ⏳

### ML Problem It Solves
> "My data has 1000 features. Which directions capture the most information?"

### The Answer
**Eigenvectors** = the most important directions in your data.
**Eigenvalues** = how important each direction is.

### The Intuition
```
Imagine your data is a cloud of points.

Eigenvector 1: The direction the cloud stretches MOST
Eigenvector 2: The perpendicular direction that stretches second-most
...

Eigenvalue: How much the cloud stretches in that direction
```

### Why ML Needs This
| Application | Why |
|-------------|-----|
| PCA | Find most important directions |
| Data compression | Keep only important directions |
| Understanding models | What patterns did model learn? |
| Stability analysis | Will training converge? |

### Real ML Application
```
Image data: 784 pixels (28×28)

Eigenvectors of covariance matrix:
- Direction 1: Overall brightness (eigenvalue: large)
- Direction 2: Horizontal gradient (eigenvalue: medium)
- Direction 784: Random noise (eigenvalue: tiny)

Keep top 50 directions → reduce 784 to 50 features!
```

### Learning Objectives
- [ ] Understand eigenvector as "important direction"
- [ ] Understand eigenvalue as "importance score"
- [ ] Calculate eigenvalues/eigenvectors for 2×2 matrix
- [ ] Connect to covariance matrix

### Estimated Sessions: 3

---

## TOPIC 18: PCA (Principal Component Analysis) ⏳

### ML Problem It Solves
> "My dataset has 1000 features. Training is slow. How do I reduce to 50 features without losing important information?"

### The Answer
**PCA** = find the most important directions (eigenvectors of covariance), project data onto them.

### The Process
1. Calculate covariance matrix of data
2. Find eigenvectors and eigenvalues
3. Sort by eigenvalue (importance)
4. Keep top k eigenvectors
5. Project data onto these k directions

### Why PCA Works
```
Original: 1000 features, but most are correlated/redundant
PCA: 50 features that capture 95% of the variance

Training on 50 features is 20× faster than 1000!
```

### Real ML Applications
| Application | How PCA Helps |
|-------------|---------------|
| Image compression | 784 pixels → 50 components |
| Visualization | 1000 dimensions → 2D plot |
| Noise reduction | Remove low-variance components |
| Feature engineering | Create uncorrelated features |

### Learning Objectives
- [ ] Explain PCA process step-by-step
- [ ] Understand "variance explained"
- [ ] Know when to use PCA
- [ ] Apply PCA to real data

### Estimated Sessions: 2

---

## TOPIC 19: SVD & Matrix Factorization ⏳

### ML Problem It Solves
> "Netflix has 100 million users and 50,000 movies. How do they recommend movies?"

### The Answer
**Matrix Factorization** = decompose huge matrix into smaller, meaningful pieces.

### The Idea
```
Users × Movies matrix (mostly empty):
    Movie1  Movie2  Movie3  ...
User1   5       ?       3
User2   ?       4       ?
User3   2       ?       5

Factor into:
Users × Features (what each user likes)
Features × Movies (what features each movie has)

"Features" = learned patterns (action, romance, etc.)
```

### SVD (Singular Value Decomposition)
```
Any matrix M = U × Σ × V^T

U: Left patterns
Σ: Importance of each pattern (diagonal)
V: Right patterns
```

### Real ML Applications
| Application | How SVD/Factorization Helps |
|-------------|----------------------------|
| Recommendations | Netflix, Spotify, Amazon |
| Topic modeling | Find topics in documents |
| Image compression | Keep only important patterns |
| Data imputation | Fill missing values |

### Learning Objectives
- [ ] Understand matrix factorization concept
- [ ] Know SVD decomposition
- [ ] Connect SVD to recommendations
- [ ] See relationship: SVD uses eigenvalue-like concepts

### Estimated Sessions: 2

---

# LAYER 7: DEBUGGING

---

## TOPIC 20: Gradient Flow Problems ⏳

### ML Problem It Solves
> "My deep network isn't learning. Loss stays flat. What's wrong?"

### The Answer
**Vanishing** or **exploding** gradients.

### Vanishing Gradients
```
Chain rule: gradient = g₁ × g₂ × g₃ × ... × g₁₀₀

If each gᵢ < 1 (e.g., 0.5):
0.5¹⁰⁰ = 0.0000000000000000000000000000008

Gradient becomes ZERO. Early layers don't learn.
```

### Exploding Gradients
```
If each gᵢ > 1 (e.g., 2):
2¹⁰⁰ = huge number

Gradient becomes INFINITY. Training explodes.
```

### Solutions
| Problem | Solution |
|---------|----------|
| Vanishing | ReLU activation, skip connections (ResNet), LSTM/GRU |
| Exploding | Gradient clipping, careful initialization, batch normalization |

### Real ML Applications
```
Why ResNet works:
- Skip connections let gradient flow directly
- gradient = direct_path + layer_path
- Even if layer_path vanishes, direct_path survives

Why LSTM replaced vanilla RNN:
- RNN: gradient passes through 100 multiplications
- LSTM: gradient has "highway" that avoids multiplications
```

### Learning Objectives
- [ ] Explain vanishing/exploding gradients mathematically
- [ ] Identify symptoms in training curves
- [ ] Know solutions for each problem
- [ ] Understand why ResNet/LSTM architectures exist

### Estimated Sessions: 2

---

# PROGRESS MILESTONES

---

## ✅ Milestone 1: Foundation Complete (ACHIEVED)
**Topics 1-5**
- Can explain how one neuron learns
- Understand data → prediction → error → update cycle

---

## 🎯 Milestone 2: Scaling Complete
**Topics 6-8 | Target: Week 14**
- Understand batch processing
- Understand deep network training
- Can explain forward and backward pass

---

## 🎯 Milestone 3: Calculus Complete
**Topics 9-11 | Target: Week 20**
- Understand gradients formally
- Know chain rule = backprop foundation
- Understand activation functions

---

## 🎯 Milestone 4: Training Complete
**Topics 12-14 | Target: Week 26**
- Know loss functions for different tasks
- Understand modern optimizers
- Can prevent overfitting

---

## 🎯 Milestone 5: Uncertainty Complete
**Topic 15 | Target: Week 29**
- Interpret model confidence
- Understand probability in ML context

---

## 🎯 Milestone 6: Data Patterns Complete
**Topics 16-19 | Target: Week 37**
- Can reduce dimensionality
- Understand recommendations
- Can analyze feature relationships

---

## 🎯 Milestone 7: Full Curriculum Complete
**Topic 20 | Target: Week 40**
- Can debug training problems
- Understand why architectures exist
- Ready for any ML paper

---

# STUDY SCHEDULE

---

## Weekly Commitment
- **2-3 hours per week** recommended
- **1 session** = ~1 hour of focused learning

## Session Strategy by Energy
| Energy | Strategy |
|--------|----------|
| 1-2 | Review previous topic, light practice |
| 3-4 | New concepts, standard pace |
| 5 | Deep dive, challenging applications |

---

# TIMELINE SUMMARY

| Layer | Topics | Weeks | Cumulative |
|-------|--------|-------|------------|
| Foundation | 1-5 | 7 | 7 ✅ |
| Scaling | 6-8 | 7 | 14 |
| Calculus | 9-11 | 6 | 20 |
| Training | 12-14 | 6 | 26 |
| Uncertainty | 15 | 3 | 29 |
| Data Patterns | 16-19 | 8 | 37 |
| Debugging | 20 | 3 | 40 |

**Total: 40 weeks (~10 months)**

---

# VALIDATION

## ML Problems Covered: 27/30 (90%)

| Category | Status |
|----------|--------|
| Making Predictions | ✅ 100% |
| Learning from Data | ✅ 100% |
| Handling Complex Data | ✅ 100% |
| Understanding Uncertainty | ✅ 83% |
| Non-Linear Learning | ✅ 100% |
| Debugging Training | ✅ 50% |

## Compared Against
- ✅ Deisenroth Textbook (Cambridge)
- ✅ Coursera (Imperial College)
- ✅ DeepLearning.AI
- ✅ CMU, MIT, UChicago syllabi

---

# DOCUMENT INFO

**Version:** 2.0

**Topics:** 20

**Estimated Time:** 40 weeks

**Last Updated:** January 2025

**Goals Supported:**
- ✅ Build education AI tools
- ✅ Understand ML for research

---
