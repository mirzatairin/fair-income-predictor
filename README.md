Fair-Income-Predictor: Mitigating Gender Bias in ML
This project demonstrates the application of Algorithmic Fairness techniques on the Adult Census Income dataset. Using the Fairlearn toolkit, I identify and mitigate gender-based disparities in salary prediction models.

🧠 The Research Problem
Machine learning models trained on historical data often inherit societal biases. In this dataset, "Gender" acts as a sensitive feature where standard models often achieve high accuracy but exhibit a significant Demographic Parity Difference, unfairly favoring male candidates for high-income predictions.

🛠️ Technical Implementation
Base Model: Random Forest Classifier (Scikit-learn).

Fairness Metric: Selection Rate & Demographic Parity.

Mitigation Strategy: Exponentiated Gradient Reduction. This approach treats the fairness constraint as a minimax optimization problem, retraining the model to satisfy parity without a catastrophic loss in accuracy.

📉 Findings & The "Trade-off"
During the development, I documented the Fairness-Accuracy Trade-off.

Unfair Model: High accuracy (~85%), but high selection disparity (18% difference).

Fair Model: Balanced selection rates (~2% difference) with a marginal drop in accuracy (~81%).

🚧 The "Struggle Log" (Technical Insights)
The development process highlighted two critical areas for future research:

Interface Friction: The separation of sensitive features from the main feature set in current toolkits creates a risk of data leakage.

Explainability Gap: While the ExponentiatedGradient mitigator achieves fairness, it functions as a "Black Box" wrapper. My goal is to move toward Explainable AI (XAI) where fairness is intrinsic to the model architecture, not just a post-hoc correction.
