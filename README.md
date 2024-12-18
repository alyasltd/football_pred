# ⚽️ Computer Vision Applied to Football

Currently in the **design phase**, this README outlines the steps and features planned for implementation. 😊

---

## **Roadmap** 🛣️

### **Phase 1: Player Detection and Initial Analysis** 🏃‍♂️⚽️

1. **YOLOv11 Fine-Tuning for Player Detection** 🎯
   - Adapt YOLOv11 for detecting football players on the field.
   - **Objective**: Ensure robust detection of players, even under challenging scenarios like crowded scenes or varying lighting conditions.

2. **Two Approaches for Team Differentiation** 📊
   - **Color Histograms for Team Identification**:
     - Extract **color histograms** from bounding box regions of detected players.
     - Cluster players into teams based on dominant uniform colors.
     - **Objective**: Provide a visually interpretable method for distinguishing teams based on color features.

   - **K-Means Clustering for Team Analysis**:
     - Use player positions (bounding box coordinates) and spatial distributions to cluster players into two teams.
     - **Objective**: Offer a complementary approach to visualizing teams, focusing on spatial and positional analysis.

3. **Bounding Box Dimension and Position Analysis** 📏
   - Analyze the following bounding box features:
     - **Dimensions**: Width and height to capture variations in player size or movement.
     - **Positions**: Relative field positions to map player activity.
   - **Objective**: Identify patterns like zones of player concentration or characteristic movement behaviors during different phases of the game.

---

### **Phase 2: Ball Tracking and Player Statistics** 🎥⚽

1. **Ball Tracking** ⚽
   - Implement tracking algorithms (e.g., **DeepSORT** or **ByteTrack**) to follow the ball's movement across frames.
   - Extract trajectories to analyze key events like passes, shots, and goals.

2. **Player Statistics** 📈
   - Extract metrics for each player, such as:
     - Distance covered.
     - Ball possession time.
     - Speed and acceleration.

---

### **Phase 3: Offside Detection** 🚩

1. **Rule-Based Offside Detection**
   - Utilize player positions and ball location to detect offside scenarios.
   - Apply rule-based AI to automate offside decision-making.

2. **Real-Time Offside Detection**
   - Develop a pipeline for real-time offside detection during live matches.

---

### **Phase 4: Goal Prediction Using Temporal Analysis** 🕒⚽

1. **Time-Series Analysis** 📈
   - Use player and ball trajectories to model temporal dependencies.
   - Train models like **LSTM** or **Transformers** to predict the likelihood of a goal at a specific moment \( t \).

2. **Conformal Prediction** 📊
   - Follow an approach inspired by **Conformal Prediction Intervals for Remaining Useful Lifetime Estimation** to quantify uncertainty in predictions.
   - Provide statistically valid prediction intervals for goal occurrence at time \( t \), ensuring high reliability.

---

## **Short-Term Work Plan** ⏳

1. **Phase 1**:
   - [ ] Fine-tune YOLOv11 for player detection.
   - [ ] Implement color histogram analysis for team differentiation.
   - [ ] Develop K-Means clustering for team visualization.
   - [ ] Perform bounding box dimension and position analysis.

2. **Phase 2**:
   - [ ] Implement ball tracking.
   - [ ] Extract detailed player statistics.

---

## **Tech Stack** 🛠️

- **Object Detection**: YOLOv11 (PyTorch).
- **Color Analysis**: OpenCV for histogram extraction.
- **Clustering**: K-Means for spatial team analysis.
- **Tracking**: DeepSORT or ByteTrack for ball tracking.
- **Time-Series Models**: LSTM or Transformers.
- **Uncertainty Quantification**: Punch library for conformal prediction.

---

## **Installation and Usage** 🚀

### **Clone the Project**
```bash
git clone https://github.com/alyasltd/football_pred.git
```

### **Install Dependencies**
```bash
pip install -r requirements.txt
```

---

### **Conclusion**
This project is still in the early stages, with exciting features planned for the coming months. Feel free to contribute or reach out for collaboration! 😊
