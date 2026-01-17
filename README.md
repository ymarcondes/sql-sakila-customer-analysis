# 💰 Análise de Clientes Sakila / Sakila Customer Analysis

## 🆕 Meu Primeiro Projeto / My First Project
**PT:** Este é meu **primeiro projeto de análise de dados com SQL**, realizado como parte do meu aprendizado em cursos da Udemy e estudo de livros de SQL, principalmente o **“Introdução à Linguagem SQL” de Thomas Nield**. O objetivo é praticar consultas avançadas, JOINs, subqueries e funções agregadas aplicadas a um cenário de negócio realista.  

**EN:** This is my **first data analysis project using SQL**, developed as part of my learning through Udemy courses and SQL books, especially **“Introduction to SQL” by Thomas Nield**. The goal is to practice advanced queries, JOINs, subqueries, and aggregate functions applied to a realistic business scenario.

---

## 📄 Descrição / Description
**PT:** Este projeto parte de um cenário fictício em que uma locadora de filmes deseja identificar seus **top spenders**, ou seja, os clientes que mais contribuem para a receita. Para isso, são realizadas análises que permitem encontrar seus nomes e IDs, a cidade em que residem, o total gasto e, ainda, classificar seus gastos como baixos, médios ou altos.  

**EN:** This project is based on a fictional scenario in which a movie rental company wants to identify its **top spenders**, that is, the customers who contribute the most to revenue. Analyses are performed to find their names and IDs, the city they live in, their total spending, and to classify their spending as low, medium, or high.

---

## 🎯 Objetivo / Goal
**PT:** Criar insights sobre o comportamento dos clientes, destacando os que gastam mais, classificando-os por faixa de gasto e filtrando aqueles que estão acima da média.  

**EN:** Generate insights on customer behavior by highlighting top spenders, classifying them by spending tiers, and filtering customers above the average.

---

## 🛠️ Tecnologias / Technologies
- **SQL / MySQL**
- **Funções agregadas / Aggregate functions:** `SUM()`, `AVG()`
- **Filtros / Filters:** `WHERE`, `HAVING`
- **Agrupamento / Grouping:** `GROUP BY`
- **Condicional / Conditional:** `CASE`
- **Subqueries**
- **JOINs múltiplos / Multiple JOINs:** `INNER JOIN`

---

## ▶️ Como executar / How to run
**PT:**
1. Abra o MySQL e selecione o banco de dados Sakila.  
2. Rode os scripts SQL de análise de clientes.  
3. Visualize os resultados e interpretações das queries.  

**EN:**
1. Open MySQL and select the Sakila database.  
2. Run the SQL scripts for customer analysis.  
3. View the query results and interpretations.

---

## ✨ Funcionalidades / Features
- **Total gasto por cliente / Total spending per customer**  
- **Classificação por faixa de gasto / Spending tier classification**  
- **Clientes acima da média / Customers above average**  
- **Pagamentos filtrados por valor mínimo / Payments filtered by minimum amount**  
- **Ranking de clientes do maior para o menor gasto / Ranking of top spenders**  
- **Possível extensão: análise por cidade ou endereço / Optional extension: analysis by city or address**

---

## 📊 Cenários de Negócio / Business Use Case
**PT:** O objetivo desta análise é auxiliar a locadora a **identificar seus melhores clientes**, permitindo ações estratégicas de marketing, fidelização e promoções personalizadas.  

**EN:** The purpose of this analysis is to help the rental company **identify its best customers**, enabling strategic marketing, loyalty programs, and personalized promotions.

---

## 📑 Estrutura das Queries / Queries Structure
1. **Total gasto por cliente** → soma dos pagamentos de cada cliente.  
2. **Classificação por faixa de gasto** → categoriza clientes em Baixo, Médio ou Alto usando `CASE`.  
3. **Clientes acima da média** → filtra clientes que gastam acima da média geral, usando subquery + `HAVING`.  
4. **Pagamentos filtrados por valor mínimo** → foca apenas em pagamentos relevantes (`WHERE amount > X`).  
5. **Ranking de clientes** → ordena do que mais gastou para o que menos gastou.  
