# fiap-tech-challenge-nps-fase1-grupo24

# 🛒 Tech Challenge – Fase 1: NPS Preditivo em E-commerce

Projeto desenvolvido como parte da Pós-Tech em AI Scientist da FIAP.

O objetivo do projeto é analisar dados operacionais de um e-commerce para identificar fatores que influenciam a satisfação dos clientes e desenvolver uma solução preditiva capaz de identificar clientes com maior risco de se tornarem detratores antes da aplicação da pesquisa de NPS.

---

# 📌 Objetivo do Projeto

O Net Promoter Score (NPS) é uma métrica utilizada para medir satisfação e lealdade dos clientes. Porém, normalmente essa informação é coletada apenas após a conclusão da jornada de compra, limitando ações preventivas.

Neste projeto buscamos responder:

**Quais fatores operacionais influenciam a satisfação do cliente e como prever clientes com maior risco de insatisfação antes da pesquisa de NPS?**

A análise permite gerar insights para áreas como:

- Logística;
- Atendimento;
- Produto;
- Estratégia comercial.

---

# 🏢 Entendimento do Problema de Negócio

O principal problema identificado é que a empresa consegue entender a insatisfação somente após o cliente responder a pesquisa.

Com uma análise preditiva, torna-se possível:

- Identificar clientes em risco;
- Antecipar problemas;
- Melhorar a experiência do consumidor;
- Criar ações preventivas.

O NPS impacta diretamente:

- **Recompra:** clientes satisfeitos possuem maior tendência de voltar a comprar;
- **Boca a boca:** promotores recomendam a marca;
- **Market Share:** uma melhor experiência aumenta competitividade.

---

# 🎯 Definição da Variável Alvo (Target)

A variável escolhida foi:

nps_score


Ela representa a satisfação do cliente em uma escala de 0 a 10.

Foi utilizada para criar a segmentação:

- 0 a 6 → Detratores
- 7 a 8 → Neutros
- 9 a 10 → Promotores

Para o modelo preditivo, o problema foi transformado em uma classificação binária:

- Detrator;
- Não detrator.

A coleta do NPS ocorre após a conclusão da jornada de compra.

Limitações:

- Pode existir viés de resposta;
- Clientes muito satisfeitos ou insatisfeitos podem responder mais;
- O NPS indica satisfação, mas não explica sozinho a causa do problema.

---

# 📂 Estrutura do Projeto


fiap-tech-challenge-nps-fase1-grupo24

- tech_challenge_nps_entrega_final.ipynb
- desafio_nps_fase_1 (2).csv
- README.md


---

# 🗃️ Base de Dados

A base contém informações relacionadas a:

### Dados do pedido
- Valor do pedido;
- Quantidade de itens;
- Forma de pagamento.

### Dados logísticos
- Tempo de entrega;
- Dias de atraso;
- Tentativas de entrega.

### Dados de atendimento
- Contatos realizados;
- Tempo de resolução;
- Reclamações.

### Satisfação
- Nota NPS do cliente.

---

# 📊 Análise Exploratória (EDA)

Foram realizadas análises para identificar fatores relacionados à satisfação:

## Distribuição do NPS

Análise da distribuição das notas e classificação entre:

- Promotores;
- Neutros;
- Detratores.

## Relação entre variáveis operacionais e NPS

Foram analisados:

- Impacto de atrasos;
- Quantidade de reclamações;
- Contatos com atendimento;
- Tempo de resolução.

## Principais fatores associados a menor satisfação

Os fatores mais críticos identificados foram:

- Atrasos na entrega;
- Maior quantidade de reclamações;
- Maior necessidade de contato com atendimento;
- Problemas sem resolução rápida.

---

# 📐 Estatística Inferencial

Foi realizado um teste de hipótese para avaliar se atrasos influenciam o NPS.

Hipóteses:

**H0:** Atrasos não impactam o NPS.

**H1:** Atrasos impactam o NPS.

Teste utilizado:

- Teste t de Student;
- Nível de significância α = 0,05.

---

# 🤖 Modelo de Machine Learning

Foi desenvolvido um modelo de classificação utilizando:

## Random Forest

Objetivo:

Prever clientes com maior probabilidade de se tornarem detratores antes da pesquisa de satisfação.

### Variáveis utilizadas:

- delivery_delay_days;
- delivery_attempts;
- customer_service_contacts;
- resolution_time_days;
- complaints_count;
- order_value;
- freight_value.

### Avaliação:

O modelo foi avaliado utilizando:

- AUC-ROC.

Também foi analisada a importância das variáveis (Feature Importance) para identificar quais fatores mais influenciam a previsão.

---

# 💡 Recomendações para o Negócio

Com base nos resultados:

### Curto prazo

- Monitorar atrasos de entrega;
- Priorizar clientes com maior risco de insatisfação;
- Melhorar velocidade de atendimento.

### Médio prazo

- Automatizar identificação de clientes críticos;
- Reduzir tempo de resolução de problemas;
- Criar ações preventivas.

---

# 🧰 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook

---

# ▶️ Como Executar

Clone o repositório:


git clone link-do-repositorio


Instale as dependências:


pip install pandas numpy matplotlib seaborn scipy scikit-learn


Execute:


jupyter notebook tech_challenge_nps_entrega_final.ipynb


Faça o upload da base:


desafio_nps_fase_1.csv


---

# 👩‍🎓 Autores

Bruna Rossi  
Daniel da Silva  
Gabrielle Dias  
Lucas Moura  
Muthiel Lorran  

Pós-Tech FIAP – AI Scientist

