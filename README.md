# Estra Pistoia Playout Opponent Probability Model

With one game left in the Serie A2 regular season, Estra Pistoia’s playout opponent is still undecided.

This project estimates the probability of Pistoia facing either **Ruvo di Puglia** or **Cento**, using a data-driven approach based on team box score data and simulation.

---

## 📊 Key Results

- **Cento: ~60% probability**
- **Ruvo: ~40% probability**

The key insight is that Pistoia’s opponent does not depend solely on their own result:

- If Pistoia win → Ruvo’s result becomes decisive  
- If Pistoia lose → Roseto’s result becomes decisive  

---

## 🧠 Methodology

The model combines basketball domain knowledge with statistical techniques:

- Team strength estimated using:
  - Offensive Rating
  - Defensive Rating
  - Recent form (last N games)

- Bergamo games are excluded, as they were annulled after the team's withdrawal

- The three decisive games are modeled:
  - Cento vs Pistoia  
  - Brindisi vs Ruvo  
  - Avellino vs Roseto  

- Win probabilities are derived from expected scoring margins

- A **Monte Carlo simulation (100,000 runs)** is used to estimate final outcomes

---

## ⚙️ How it works

1. Load team box score data from CSV  
2. Convert game data into team-level metrics  
3. Compute possession-based ratings  
4. Estimate win probabilities for key games  
5. Apply official scenario rules  
6. Simulate outcomes  

---

## 📁 Project Structure
