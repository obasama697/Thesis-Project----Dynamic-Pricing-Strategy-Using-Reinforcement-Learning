# Dynamic Pricing Strategy Using Reinforcement Learning for Indian Airlines

![MBA Thesis](https://img.shields.io/badge/Project-MBA%20Thesis-blue?style=flat-square&logo=university)
![Reinforcement Learning](https://img.shields.io/badge/Method-RL%20DQN%20BDQN-orange?style=flat-square&logo=python)
![Airline Industry](https://img.shields.io/badge/Domain-Indian%20Airlines-red?style=flat-square)
![License](https://img.shields.io/badge/License-CC%20BY%20NC%204.0-green?style=flat-square)

## 📄 Overview

Master's thesis investigating **deep reinforcement learning (DQN, BDQN)** for dynamic pricing in the Indian airline industry. Models patient/strategic customer behavior using a Markov Decision Process (MDP) framework that incorporates historical price sequences and customer patience levels.

## 🎓 Author & Institution
**Rupal Tripathi**  
*Supervised by Dr. Amandeep Kaur*  
**ABV IIITM Gwalior** 

## 🔬 Research Objectives
- Develop RL-based dynamic pricing accounting for **strategic customers** who delay purchases
- Compare DQN vs Bootstrapped DQN (BDQN) performance
- Analyze Indian airline pricing regulations (DGCA/MoCA)
- Validate against real Indian domestic flight data 

## 🛠️ Methodology

MDP Framework: State(q, l, H), Action(Price), Reward(Revenue)
├── Patient Customer Model (patience T∈[0,W])
├── Historical Price Vector (at-W, ..., at-1)
├── Non-stationary Demand (Leisure/Business segments)
└── Real Indian Airline Dataset (10,683 flights)


**Key Algorithms:**
- Deep Q-Network (DQN)
- Bootstrapped DQN (BDQN)

## 📊 Key Findings

| Scenario | BDQN Revenue | DQN Revenue | Optimal Bound |
|----------|--------------|-------------|---------------|
| T=20 Patient | 72.68 | 71.24 | 74.45 |
| T=40 Patient | **144.45** | 141.32 | 149.8 |
| Myopic (T=40) | 120.04 | 119.94 | - |

**Pricing Strategy:** Airlines should **alternate high/low prices** rather than monotonic increases when facing patient customers

## 💡 Practical Insights
- **High prices** → High-WTP business travelers
- **Strategic low prices** → Fill remaining inventory
- **Route analysis**: Bangalore-Delhi (₹3K-₹26K range)
- **Carrier pricing**: Legacy > LCC airlines

## 📈 Real-World Validation
Price Trends (Indian Domestic):
├── Nonstop: ₹5,024 avg
├── 1-Stop: ₹10,594 avg
├── 2-Stop: ₹12,716 avg
└── IndiGo LCC: ₹3.8K-₹5K median

Wide price dispersion validates need for **dynamic pricing**

## 📚 Repository Contents
├── Research_Paper_MBA15.pdf # Complete thesis
├── code/ # RL implementation (if available)
├── data/ # Indian airline dataset
└── figures/ # MDP diagrams & results


## 🔄 How to Use
1. Read `Research_Paper_MBA15.pdf` for complete methodology
2. Reproduce experiments using provided hyperparameters
3. Apply BDQN model to airline revenue management systems
4. Consider DGCA regulations for production deployment

## 📖 Citation
@mastersthesis{tripathi2025,
title={Dynamic Pricing Strategy Using Reinforcement Learning for Indian Airlines},
author={Tripathi, Rupal and Kaur, Amandeep},
year={2025},
school={ABV-IIITM Gwalior}
}


## ⚖️ License
**Creative Commons Attribution-NonCommercial 4.0** - Academic use only
