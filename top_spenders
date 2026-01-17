USE sakila;

-- Seleciona clientes que gastaram acima da média
SELECT
    c.customer_id,      -- ID do cliente
    c.first_name,       -- Nome do cliente
    c.last_name,        -- Sobrenome do cliente
    ci.city,            -- Cidade do cliente
    SUM(p.amount) AS total_gasto,  -- Soma total dos pagamentos do cliente

    -- Classifica cada cliente em faixa de gasto
    CASE 
        WHEN SUM(p.amount) > 150 THEN 'ALTO'
        WHEN SUM(p.amount) BETWEEN 75 AND 150 THEN 'MÉDIO'
        ELSE 'BAIXO'
    END AS faixa_gasto

FROM customer AS c
JOIN payment AS p 
    ON c.customer_id = p.customer_id  -- Relaciona cliente com seus pagamentos
JOIN address AS a
    ON c.address_id = a.address_id   -- Relaciona cliente com endereço
JOIN city AS ci
    ON a.city_id = ci.city_id        -- Relaciona endereço com cidade

-- Filtra apenas pagamentos relevantes
WHERE p.amount > 2

-- Agrupa por cliente e cidade para calcular total gasto
GROUP BY 
    c.customer_id,
    c.first_name,
    c.last_name,
    ci.city

-- Mantém apenas clientes que gastaram acima da média geral
HAVING SUM(p.amount) > (
    SELECT AVG(total_cliente)
    FROM (
        SELECT SUM(amount) AS total_cliente
        FROM payment
        WHERE amount > 2
        GROUP BY customer_id
    ) AS medias
)

-- Ordena do cliente que mais gastou para o que menos gastou
ORDER BY total_gasto DESC;
