# Causal Machine Learning

## Python, LLMs, and the Science of Computational Skepticism

### Preface: The Asymmetry of Bullshit in the Age of AI

* Why "Big Data" often leads to big delusions.
* The Trilateral Workflow: Python for scale, LLMs for exploration, and Causal Logic for verification.

---

### Part I — Foundations: Statistical vs. Causal Thinking

**Chapter 1: Preliminaries of Causal Modeling**

* 1.1 Why Study Causation? (The "Causal Revolution").
* 1.2 The Ladder of Causation: Seeing, Doing, Imagining.
* 1.3 Simpson’s Paradox: The "Bad-Bad-Good" Drug and Berkeley Admissions.
* 1.4 Structural Causal Models (SCMs) vs. Regression Models.
* 1.1 Why Study Causation? (The "Causal Revolution").
* 1.2 The Ladder of Causation: Seeing, Doing, Imagining.
* 1.3 Simpson’s Paradox: The "Bad-Bad-Good" Drug and Berkeley Admissions.
* 1.4 Structural Causal Models (SCMs) vs. Regression Models.
* **Exercises:** Python Colab: Simulating Simpson’s Paradox with TSLA and NVDA data.



Understood. Focusing strictly on the specific modules you listed, here is the structured outline for **Chapter 2: Potential Outcomes and Counterfactuals**, modeled directly after your Chapter 1 format.

---

## **Chapter 2: Potential Outcomes and Counterfactuals**

### **2.1 The Fundamental Problem of Causal Inference**

We introduce the concept of "missing data" as the heart of causation. For any individual, we observe the outcome under treatment *or* control, but never both.

* **The Potential Outcomes Framework:** Defining  and .
* **The Counterfactual:** The "what if" that exists only in theory but drives our causal logic.

### **2.2 Hypothetical Interventions and the -operator**

Moving beyond passive observation. We define an intervention as a targeted manipulation of the system.

* **Seeing vs. Doing:** Why  (conditional probability) is not the same as  (interventional probability).
* **Graph Surgery:** How an intervention physically removes the influence of prior causes on the treated variable.

### **2.3 Defining and Measuring Causal Effects**

How do we quantify the "gap" between the two worlds?

* **Individual Treatment Effect (ITE):** .
* **Average Treatment Effect (ATE):** The expected value of the difference across the population: .
* **Relative vs. Absolute Effects:** Interpreting the magnitude of change.

### **2.4 Causal Assumptions and SUTVA**

To bridge the gap between observed data and causal truth, we must rely on "Stable Unit Treatment Value Assumptions."

* **No Interference:** One person's treatment doesn't affect another's outcome.
* **Consistency:** The treatment is uniform (no "hidden" versions of the drug).
* **Exchangeability:** The idea that the treated and untreated groups are comparable.

### **2.5 Stratification: The Path to Comparability**

When groups aren't naturally exchangeable, we force it.

* **Sub-group Analysis:** Breaking the population into "strata" (e.g., age, income, ticker volatility) where the treatment assignment is "as good as random."
* **Weighted Averages:** Recombining strata to estimate the population-level effect.

---

### **Exercises: Python Colab**

**Simulating Counterfactuals with Market Interventions.**

* **Task:** Use Python to simulate a "Flash Crash" intervention.
* **Objective:** Compare the observed price of a stock (e.g., NVDA) during a liquidity crisis against a simulated "counterfactual" where a circuit breaker (intervention) was never triggered.

---

### **Learning Modules**

* **Potential Outcomes and Counterfactuals**
* *Video. Duration: 13 min*


* **Hypothetical Interventions**
* *Video. Duration: 17 min*


* **Causal Effects**
* *Video. Duration: 19 min*


* **Practice Quiz: The Logic of the Counterfactual**
* *Practice Assignment. Duration: 30 min*


* **Causal Assumptions: SUTVA and Exchangeability**
* *Video. Duration: 18 min*


* **Stratification: Adjusting for the Difference**
* *Video. Duration: 15 min*



**Chapter 2: Probability and Statistics Essentials for AI**

* 2.1 Variables, Events, and Distributions.
* 2.2 Conditional Probability and the "Given That" Operator.
* 2.3 Bayes’ Rule: Updating Beliefs in Response to Evidence.
* 2.4 Expected Values, Variance, and Covariance in Financial Data.
* 2.5 Multiple Regression: The Standard Tool for Pattern Matching.
* **Exercises:** LLM Triangulation: Comparing how three models derive the Sharpe Ratio.

---

### Part II — Graphical Models: The Logic of DAGs

**Chapter 3: Principles of Causal Graphs**

* 3.1 The Anatomy of a DAG (Directed Acyclic Graph).
* 3.2 The Three Fundamental Junctions:
* **Chains:** Mediation and the screening-off effect.
* **Forks:** Common causes and confounding.
* **Colliders:** Selection bias and the "Explain Away" effect.


* 3.3 d-separation: Defining Conditional Independence.
* **Exercises:** Python: Identifying testable implications from a graph using `DoWhy`.

**Chapter 4: Causal Discovery and Model Testing**

* 4.1 Connecting Graphs to Data Distributions.
* 4.2 Causal Search: Constraint-based (PC) vs. Score-based (GES) algorithms.
* 4.3 Falsifying Causal Assumptions: When the data says the graph is wrong.
* **Exercises:** Lab: Recovering the "True" graph from noisy financial time series.

---

### Part III — Estimating Causal Effects: The "Do" Operator

**Chapter 5: The Logic of Interventions**

* 5.1 The "Do" Operator: Simulating a Randomized Experiment.
* 5.2 Confounding and the Backdoor Criterion.
* 5.3 The Front-Door Criterion: Finding effects with unmeasured variables.
* 5.4 The Adjustment Formula and the Truncated Product Rule.
* **Exercises:** Python: Comparing "Seeing"  vs. "Doing"  in a Colab simulation.

**Chapter 6: Advanced Identification Strategies**

* 6.1 Instrumental Variables: "Nature’s Experiments" and Mendelian Randomization.
* 6.2 Selection Bias: Recovering from non-random sampling (M-Bias).
* 6.3 The ID Algorithm: The universal test for identifiability.
* **Exercises:** LLM Triangulation: Drafting prompts to find the "Weak Instrument" problem in economic data.

---

### Part IV — Causal Machine Learning: Data Balancing

**Chapter 7: Matching and Propensity Scores**

* 7.1 Observational Studies and the Quest for Balance.
* 7.2 Greedy (Nearest-Neighbor) vs. Optimal Matching.
* 7.3 Assessing Balance: Standardized Mean Differences (SMD).
* 7.4 Sensitivity Analysis: How robust is your match?
* **Exercises:** Python Lab: Using `MatchIt` logic to balance tech stock volatility.

**Chapter 8: Weighting and Causal ML Robustness**

* 8.1 Inverse Probability of Treatment Weighting (IPTW).
* 8.2 Doubly Robust Estimators: Combining regression and weighting.
* 8.3 **[CausalML Special]** Balancing for Supervised Learning:
* The Majority Gravity Well: Why Global Loss erases minority patterns.
* Causal Data Augmentation: Re-centering AI worldview with Propensity Weights.
* Covariate Shift: Ensuring model transportability across environments.


* **Exercises:** Colab: Stress-testing a classifier by re-weighting a biased training set.

---

### Part V — Counterfactuals: Individual-Level "What If"

**Chapter 9: The Algorithmization of Counterfactuals**

* 9.1 Defining Potential Outcomes: .
* 9.2 The Fundamental Law of Counterfactuals.
* 9.3 The Three Steps: Abduction, Action, Prediction.
* 9.4 Nondeterministic Counterfactuals and Probabilities of Causation.
* **Exercises:** Python: Estimating "The Effect of Treatment on the Treated" (ETT).

**Chapter 10: Practical Mediation and Attribution**

* 10.1 Mediation: Direct vs. Indirect Effects.
* 10.2 The Mediation Formula: Escaping Linear Wonderland.
* 10.3 Legal and Ethical Applications: Discrimination and Climate Attribution.
* 10.4 Necessary vs. Sufficient Causation: The "But-For" Test.
* **Exercises:** LLM Triangulation: Critiquing a model's attribution of a "Market Crash" to a specific event.

---

### Part VI — The Future of Causal AI

**Chapter 11: Transportability and Generalization**

* 11.1 The External Validity Problem: Why Boston isn't Nashville.
* 11.2 S-Nodes: Identifying what changes between populations.
* 11.3 Data Fusion: Combining experimental and observational results.

**Chapter 12: Strong AI, Agency, and Skepticism**

* 12.1 The Limits of Opaque Systems (Deep Learning).
* 12.2 Building a Causal Reasoning Module for Machines.
* 12.3 Free Will as a Computational Necessity for Moral AI.
* 12.4 Conclusion: You are Smarter Than Your Data.

---

### Back Matter

* **Appendix A:** Python Causal Library Guide (`DoWhy`, `CausalML`, `EconML`).
* **Appendix B:** Effective LLM Prompts for Causal Discovery.
* **Appendix C:** The Skeptic’s Checklist for Peer Review.
* **Glossary, References, and Index.**

\?
