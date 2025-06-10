# Open-Recall Analytics 🚛🔧

> **Transforme dados públicos de *recall* em insights de confiabilidade para frotas pesadas – com ajuda do Codex para gerar e documentar todo o pipeline.**

---

## ✨ Principais recursos
| Módulo | O que faz |
|--------|-----------|
| **Ingestão automática** | Faz download diário do dataset de *recalls* da NHTSA, descompacta e normaliza os CSVs. |
| **EDA interativo** | Dashboard Streamlit (Plotly) filtra por fabricante, componente, classe 7/8, etc., com estatísticas agregadas. |
| **Métrica _Recall Velocity_** | Calcula *recalls/ano* após o lançamento para ranquear criticidade. |
| **Preditor de risco** | Classificador (XGBoost) estima a probabilidade de *recall* para novos modelos. |
| **Relatório one-click** | Gera PDF/Markdown com resumo executivo, gráficos e apêndice de código. |
| **Codex Copilot** | Função que cria ou ajusta trechos de ETL/ML a partir de *prompts*. |

---

## 🗂️ Fontes de dados

* **NHTSA Safety Recalls** – arquivos `.zip` atualizados diariamente, com lista de campanhas desde 1966. :contentReference[oaicite:0]{index=0}  
* (Opcional) NASA Turbofan Degradation (para exemplo de RUL).  

---

## ⚙️ Tecnologias

* Python 3.11 · Pandas · Plotly · Scikit-learn  
* Streamlit Cloud (deploy)  
* OpenAI Python SDK (Codex)  
* Docker · GitHub Actions (CI/CD)  

---

## 🚀 Instalação rápida

```bash
# 1. clone
git clone https://github.com/<seu-user>/open-recall-analytics.git
cd open-recall-analytics

# 2. configure env
cp .env.example .env           # edite e adicione OPENAI_API_KEY

# 3. build & run
docker compose up --build      # ou: pip install -r requirements.txt && streamlit run app.py
