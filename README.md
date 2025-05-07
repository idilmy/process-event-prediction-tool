# Process Event Prediction Tool

This project forecasts upcoming events in business processes using real-world banking event logs. Developed as part of the DBL2I010 course at Eindhoven University of Technology, the tool supports suffix prediction using baseline classifiers, Random Forest, and LSTM-based sequence models.

## Overview

The tool operates on XES-formatted event logs and provides:

- Preprocessing and cleaning of banking logs  
- Training of multiple predictive models (LSTM, Random Forest, baseline)  
- Evaluation of predictions using suffix accuracy, trace similarity, and other metrics  
- Reproducible results using consistent train/test splits

## Models Implemented

- **Baseline Predictor**: Predicts next events using naive frequency methods  
- **Random Forest Classifier**: Predicts future activities based on extracted features  
- **LSTM Model**: Learns sequential dependencies from trace history  

## Project Structure

```
clean.py                         # Data preparation and cleaning  
train_suffix_prediction.py      # Main training pipeline  
lstm_model.py                   # LSTM model structure  
lstm_prediction.py              # LSTM inference code  
rf_event_prediction.py          # Random Forest training and prediction  
evaluate_rf_event_prediction.py # RF evaluation logic  
baseline.py                     # Naive baseline predictor  
run_suffix_prediction.py        # Script to execute all models  
train.xes                       # Training event log  
test.xes                        # Test event log  
```

## How to Run

1. Install required packages (e.g., `pm4py`, `scikit-learn`, `keras`, `pandas`).

2. Run the full suffix prediction pipeline:

```bash
python run_suffix_prediction.py
```

3. To run models individually:

```bash
python train_suffix_prediction.py
python rf_event_prediction.py
python lstm_model.py
```

4. Evaluation output is printed to console and optionally saved as `.csv` for review.

## Input Data

The tool uses XES-formatted event logs.  
Files included:
- `train.xes`: training log  
- `test.xes`: test log  

These logs contain sequences of banking events extracted for suffix prediction tasks.

## Authors

Project by Group 19  
Maintained by **Idil Mısra Yılmaz**  
Eindhoven University of Technology
