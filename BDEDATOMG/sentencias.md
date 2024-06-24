
## 1. VIEWS full_name table client
CREATE VIEW invoice_view AS
SELECT 
    i.id,
    i.code,
    i.create_at,
    i.total,
    c.full_name
FROM 
    invoice i
JOIN 
    client c ON i.client_id = c.id;

pARA VISUALIZAR
    SELECT * FROM invoice_view;


  - Captura:

<img src="![alt text](image.png)"/>
<img src="![alt text](image-1.png)"/>

## detail views description table product
  - Sentencia:
-- Crear la vista invoice_view
CREATE VIEW invoice_view AS
SELECT 
    i.id,
    i.code,
    i.create_at,
    i.total,
    c.full_name
FROM 
    invoice i
JOIN 
    client c ON i.client_id = c.id;

-- Crear la vista detail_view
CREATE VIEW detail_view AS
SELECT 
    d.id,
    d.quantity,
    p.description,
    d.price,
    d.subtotal
FROM 
    detail d
JOIN 
    product p ON d.product_id = p.id;

  SELECT ..

  - Captura:

<img src="![alt text](image-1.png)" alt="drawing" width="500"/>
