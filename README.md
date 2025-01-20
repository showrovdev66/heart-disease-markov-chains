# Heart Disease Progression Analysis Using Markov Chains

## Project Overview
Heart disease remains one of the leading causes of death worldwide. By simulating the progression of heart disease states using Markov Chains, this project provides a framework for understanding disease dynamics and testing the impact of interventions. The simulation is based on real-world data and incorporates sensitivity analysis to assess the effects of recovery and progression rates.

## Key Features
- Defined four states of disease progression (Healthy, At Risk, Disease Progression, Death).
- Built a transition matrix from real-world data to simulate state changes.
- Simulated disease progression over 20 time steps.
- Conducted sensitivity analysis on two intervention strategies:
  - Improving recovery rates (State 1 → State 0).
  - Slowing disease progression (State 2 → State 3).
- Visualized results using line plots and heatmaps.
- Quantitatively analyzed the impact of interventions.

## Technologies Used
- Python
- Libraries: Pandas, NumPy, Matplotlib, Seaborn

## Setup and Installation
1. Clone the repository:
   ```
   git clone https://github.com/username/heart-disease-markov-chains.git
   ```
2. Navigate to the project directory:
   ```
   cd heart-disease-markov-chains
   ```
3. Install the required Python packages:
   ```
   pip install -r requirements.txt
   ```
4. Run the main script:
   ```
   python src/markov_chain_model.py
   ```

## Dataset
The dataset used in this project was obtained from [Kaggle's Heart Disease Dataset](https://www.kaggle.com/). It contains information on patient demographics, medical measurements, and heart disease diagnoses. 

### Key Attributes:
- `age`: Age of the patient.
- `sex`: Gender (1 = male, 0 = female).
- `cp`: Chest pain type (0–3, where higher values indicate more serious symptoms).
- `trestbps`: Resting blood pressure (in mm Hg).
- `chol`: Serum cholesterol (in mg/dl).
- `fbs`: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false).
- `restecg`: Resting electrocardiographic results (0–2).
- `thalach`: Maximum heart rate achieved.
- `exang`: Exercise-induced angina (1 = yes, 0 = no).
- `oldpeak`: ST depression induced by exercise relative to rest.
- `slope`: The slope of the peak exercise ST segment (0–2).
- `ca`: Number of major vessels (0–3) colored by fluoroscopy.
- `thal`: Type of defect (1 = fixed defect, 2 = reversible defect, 3 = normal).
- `target`: Presence of heart disease (1 = disease, 0 = no disease).

Please refer to the dataset's [license](https://www.kaggle.com/) for terms of use.

## How It Works
1. **State Definitions**: The project models four states:
   - State 0: Healthy (No disease).
   - State 1: At Risk (elevated health markers).
   - State 2: Disease Progression.
   - State 3: Death (absorbing state).

2. **Transition Matrix**: Probabilities of transitioning between states are calculated from the dataset.

3. **Markov Chain Simulation**:
   - Simulates 20 time steps starting with a predefined initial distribution.

4. **Sensitivity Analysis**:
   - Higher recovery rates: Simulated improved transitions from State 1 to State 0.
   - Slower progression: Simulated reduced transitions from State 2 to State 3.

5. **Visualization**:
   - Line plots for state distributions over time.
   - Heatmap for transition probabilities.

## Results and Outcomes
1. **Baseline Simulation**:
   - Proportion of healthy individuals (State 0) decreases over time.
   - Deaths (State 3) increase steadily, reflecting the natural progression of heart disease.

2. **Higher Recovery Rates**:
   - Increased the proportion of healthy individuals (State 0) by 1.0%.
   - Reduced the proportion of deaths (State 3) by 0.88%.

3. **Slower Disease Progression**:
   - Increased the proportion of healthy individuals (State 0) by 1.78%.
   - Reduced the proportion of deaths (State 3) by 4.4%.

4. **Key Insights**:
   - Slowing disease progression has a more significant impact than improving recovery rates.
   - Effective interventions can reduce mortality and prolong time spent in less severe states.

## Future Work
1. Combine recovery rate improvements with slower progression for a more comprehensive intervention.
2. Perform a cost-effectiveness analysis to prioritize strategies.
3. Extend the model to include additional health variables (e.g., lifestyle factors, medications).
4. Test the model with a larger and more diverse dataset.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
