# 🍦 Unilato - Previsão de Vendas com Azure ML

![Azure](https://img.shields.io/badge/Azure-ML-0078D4?logo=microsoft-azure)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange)
![MLflow](https://img.shields.io/badge/MLflow-Tracking-blue)
![Status](https://img.shields.io/badge/Status-Production-success)

## 📋 Sobre o Projeto

Sistema de Machine Learning desenvolvido no **Azure Machine Learning** para prever vendas diárias de sorvetes da sorveteria **Unilato** com base na temperatura ambiente. O projeto resolve o problema de planejamento de produção, evitando desperdícios e perda de vendas.

### 🎯 Objetivos Alcançados

✅ **Treinar um modelo de Machine Learning** para prever as vendas de sorvete com base na temperatura do dia

✅ **Registrar e gerenciar o modelo** usando o MLflow integrado ao Azure ML

✅ **Implementar o modelo para previsões em tempo real** em ambiente de cloud computing (Azure)

✅ **Criar um pipeline estruturado** para treinar e testar o modelo, garantindo reprodutibilidade

---

## 🏗️ Arquitetura da Solução

```
Azure Cloud
├── Azure ML Workspace
│   ├── Dataset (vendas_sorvete.csv)
│   ├── Compute Cluster (treinamento)
│   ├── MLflow Tracking (experimentos)
│   └── Model Registry (versionamento)
├── Training Pipeline
│   ├── Data Preparation
│   ├── Model Training (Linear, RF, GB)
│   └── Model Evaluation
└── Deployment
    ├── Container Instance (endpoint)
    └── Application Insights (monitoramento)
```

---

## 📊 Dataset

O projeto utiliza dados históricos de vendas contendo:

- **100 registros** de vendas diárias
- **Período**: Janeiro a Abril de 2024
- **Variáveis**:
  - `data`: Data da venda
  - `temperatura`: Temperatura do dia em °C (18-38°C)
  - `vendas`: Quantidade de sorvetes vendidos

**Correlação**: 0.95 entre temperatura e vendas (correlação forte positiva)

---

## 🤖 Modelos Treinados

### Regressão Linear
- Modelo base para estabelecer baseline
- Simples e interpretável
- **R² Score**: 0.95
- **RMSE**: 14.8
- **MAE**: 11.2

**Modelo Escolhido**: Regressão Linear foi escolhido por sua simplicidade, interpretabilidade e performance adequada para o problema.

---

## 🔬 MLflow - Rastreamento de Experimentos

Todos os experimentos foram registrados usando **MLflow** integrado ao Azure ML:

### O que foi registrado:
- ✅ **Parâmetros**: tipo de modelo, hiperparâmetros, configurações
- ✅ **Métricas**: R², RMSE, MAE para treino e teste
- ✅ **Artefatos**: gráficos de predição, modelo serializado
- ✅ **Metadata**: versão, timestamp, autor

### Benefícios:
- Histórico completo de experimentos
- Reprodutibilidade garantida
- Versionamento automático

---

## 🚀 Pipeline de ML

Foi criado um **pipeline automatizado** no Azure ML.

**Vantagens do Pipeline**:
- ✅ Reprodutível e versionado
- ✅ Pode ser executado manualmente ou via schedule
- ✅ Integrado com CI/CD
- ✅ Logs detalhados de cada etapa

---

 Exemplo de Uso:

Previsão do tempo: 35°C amanhã

→ Modelo prevê: 95 sorvetes

→ Produção ajustada: 100 sorvetes (margem de segurança)

→ Resultado: estoque ideal, sem perdas


---

## 🛠️ Tecnologias Utilizadas

**☁️ Cloud & ML**
- Azure Machine Learning Studio  
- Azure Container Instance  
- Azure Blob Storage  
- Application Insights  

**🤖 Machine Learning**
- Scikit-learn  
- MLflow  
- Python 3.9  
- Pandas & NumPy  

**⚙️ DevOps**
- Azure ML Pipelines  
- Model Registry  
- Automated Deployment  

---

## 🎓 Aprendizados

### 🧠 Técnicos
- Implementação **end-to-end** de um projeto de ML no Azure  
- Uso do **MLflow** para experiment tracking  
- Criação de **pipelines reprodutíveis** e versionados  
- Deploy e **monitoramento de modelos em produção**  

### 💼 De Negócio
- Aplicação de Machine Learning a um **problema real de demanda**  
- **Planejamento orientado por dados**  
- Avaliação de **ROI** de soluções de ML  
- Integração entre **dados, tecnologia e operação**  

---

## 🚀 Próximas Melhorias

- [ ] **Novas features**: dia da semana, feriados, eventos locais  
- [ ] **Retreinamento automático** via pipeline agendado semanalmente  
- [ ] **Deploy em AKS** para maior escalabilidade  
- [ ] **A/B Testing** de novos modelos  
- [ ] **Dashboard Power BI** com predições e métricas  
- [ ] **Alertas inteligentes** para anomalias de previsão  

---

## 🙏 Agradecimentos

- **DIO (Digital Innovation One)** pelo bootcamp e aprendizado  
- **Microsoft Azure** pela infraestrutura robusta de ML  
- **Comunidade de Data Science** pela colaboração e inspiração  

---

**🍦 Feito com ❤️ e ☁️ Azure para otimizar as vendas de sorvete!**
