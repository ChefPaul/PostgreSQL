--What is the proof per dollar of whisky? Sort and show top 30?
SELECT *, CAST(CAST(proof AS numeric) / CAST(bottle_price AS numeric) AS numeric(10,2)) as proof_per_dollar 
FROM products WHERE CAST(bottle_price AS numeric) > 0 AND category_name ILIKE '%WHISK%'
ORDER BY proof_per_dollar DESC LIMIT 30;

SELECT item_no, item_description, CAST(CAST(proof AS numeric) / CAST(bottle_price AS numeric) AS numeric(10,2)) as proof_per_dollar 
FROM products WHERE CAST(bottle_price AS numeric) > 0 AND category_name ILIKE '%WHISK%'
ORDER BY proof_per_dollar DESC LIMIT 30;

--Check the bottle price for all of the Tequila sold in Adams County.
SELECT *, total / bottle_qty AS price_check
FROM sales WHERE category_name ILIKE '%TEQUILA%' AND county ILIKE '%ADAM%' LIMIT 100;

SELECT *, ((total / bottle_qty)-CAST(btl_price AS numeric)) AS price_check
FROM sales WHERE category_name ILIKE '%TEQUILA%' AND county ILIKE '%ADAM%' LIMIT 100;

--We want to know how many bottles are in each line item of products table. Calculate the number of bottles manually by multiplying pack and inner pack. 
SELECT *, (pack * inner_pack) AS bottles FROM products;
