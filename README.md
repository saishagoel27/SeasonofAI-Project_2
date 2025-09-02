# 🖼️ CIFAR-10 Image Classification with CNN
*Teaching computers to see the difference between cats and dogs (and 8 other things)*

A beginner-friendly dive into image classification using Convolutional Neural Networks. We take 32x32 pixel images and teach a computer to recognize what's in them.

##  What This Does

Classifies tiny images into 10 categories:
- ✈️ Airplane  
- 🚗 Automobile  
- 🐦 Bird  
- 🐱 Cat  
- 🦌 Deer  
- 🐕 Dog  
- 🐸 Frog  
- 🐴 Horse  
- 🚢 Ship  
- 🚚 Truck  

**The Goal:** Build a CNN that can look at a 32x32 image and correctly identify what object it contains.

## 📁 What's Inside

```
├── Untitled.ipynb          # Main notebook with all the code
└── README.md              # You're reading it
```

## 🚀 Quick Start

```bash
# Open the notebook and run all cells
jupyter notebook Untitled.ipynb
```

That's it! The notebook handles everything from data loading to training.

## 🧠 The Learning Journey

### Step 1: Data Exploration
- **50,000 training images** + **10,000 test images**
- Each image is 32×32 pixels with RGB colors
- Normalized pixel values (0-1) for better training

### Step 2: Model Comparison
We build and compare two approaches:

#### Simple Neural Network (ANN)
- Flattens images into 3,072 numbers
- Two hidden layers (3000 → 1000 → 10)
- **Result:** ~48% accuracy

#### Convolutional Neural Network (CNN)
- Preserves spatial relationships in images
- Conv2D → MaxPool → Conv2D → MaxPool → Dense
- **Result:** ~67% accuracy

## 📊 Results

| Model Type | Accuracy | Why It Works |
|------------|----------|--------------|
| **Simple ANN** | 48% | Treats images as flat data |
| **CNN** | 67% | Understands image patterns |

**Key Insight:** CNNs are much better at image tasks because they understand that nearby pixels are related to each other.

## 🔧 Architecture Breakdown

### CNN Structure:
```python
Conv2D(32 filters, 3×3) → ReLU → MaxPool(2×2)
Conv2D(64 filters, 3×3) → ReLU → MaxPool(2×2)
Flatten → Dense(64) → Dense(10, softmax)
```

**What this means:**
- **Conv2D layers** detect features like edges and shapes
- **MaxPool layers** reduce image size while keeping important info
- **Dense layers** make the final classification decision

## 🎮 Try It Yourself

1. **Run the notebook** - see how both models perform
2. **Modify the CNN** - try adding more layers or filters
3. **Experiment with epochs** - train for longer/shorter periods
4. **Test predictions** - see what the model thinks about specific images

## 🤔 What You'll Learn

- **CNNs vs ANNs**: Why structure matters for images
- **Feature Detection**: How computers "see" edges, shapes, and patterns
- **Model Evaluation**: Reading accuracy and loss metrics
- **Overfitting**: Why more complex isn't always better

## 💡 Fun Facts

- CIFAR-10 images are tiny (32×32) - about the size of a postage stamp
- State-of-the-art models can achieve 99%+ accuracy on this dataset
- The dataset was created by collecting images from the web and manually labeling them

## 🛠️ Tech Stack

- **TensorFlow/Keras** - Deep learning framework
- **NumPy** - Array operations  
- **Matplotlib** - Visualizations
- **Python** - Because it's awesome

## 🎯 Next Steps

Want to improve the model? Try:
- [ ] More convolutional layers
- [ ] Different optimizers (Adam, RMSprop)
- [ ] Data augmentation (flips, rotations)
- [ ] Batch normalization
- [ ] Dropout for regularization

## 🤷‍♀️ Common Questions

**Q: Why is the accuracy not higher?**  
A: We kept it simple! Real-world models use much deeper networks and advanced techniques.

**Q: Can I use my own images?**  
A: Yes! Just resize them to 32×32 and normalize the pixels.

**Q: What's the difference between accuracy and loss?**  
A: Accuracy = % of correct predictions. Loss = how "wrong" the model is (lower is better).

---

*A simple exploration of computer vision fundamentals. Perfect for understanding how machines learn to see! 👁️*
