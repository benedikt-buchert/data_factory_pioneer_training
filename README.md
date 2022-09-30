# data_factory_pioneer_training

Create Table to write Data
```
DROP TABLE IF EXISTS retail;
CREATE TABLE retail (
    id SERIAL NOT NULL,
    stock_code VARCHAR(255),
    invoice_no VARCHAR(255),
    created_at TIMESTAMPTZ NOT NULL DEFAULT NOW(),
    modified_at TIMESTAMPTZ NOT NULL DEFAULT NOW(),
    invoice_date DATE,
    quantity smallint,
    PRIMARY KEY(id)
);
```

Show all values in table:
```
SELECT *
FROM retail
ORDER BY invoice_date DESC;

Insert new test value into DB:
```
INSERT INTO retail(stock_code, invoice_no, invoice_date, quantity)
VALUES ('580137', '10002', '2022-01-01', 5);
```
