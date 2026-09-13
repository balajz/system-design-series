select * from employers where uuid = 'e3fef320-1150-4838-9f8e-86edb2fd1687';
select * from users where uuid = 'c013448a-3b4d-4789-9bfb-cda23338f3e0';



### INDEXES: THE TRADE-OFF

|Benefits|Costs|
|---|---|
|Faster reads|Slower writes|
|Faster lookups|More storage|
|Avoids full table scans|More memory usage|
|Great for selective queries|Can be wasteful for low-cardinality columns|

---

**Write Amplification**

`INSERT / UPDATE / DELETE`  
→ Table update + Index update

**Bottom line:**  
**Index what you query. Don't index everything.**