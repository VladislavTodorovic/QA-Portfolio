**SQL Requests**

1. Ispišite ime, prezime, patronus svih likova koji imaju patronusa i on je poznat.  
   SELECT fname, lname, patronus  
   FROM characters  
   WHERE NOT  patronus \= 'Unknown' and patronus IS NOT NULL;  
2. Ispišite prezime likova čije prezime završava slovom 'e'.  
   SELECT lname  
   FROM characters  
   WHERE lname like '%e';  
3. Izračunajte ukupne godine svih likova i ispišite to na ekran.

	SELECT SUM(age)  
FROM characters;

4. Ispišite ime, prezime i godine likova po opadajućem redosledu njihovih godina.  
   SELECT fname, lname, age  
   FROM characters  
   ORDER BY age DESC;  
5. Ispišite ime likova i godine onih čije godine su u rasponu od 50 do 100 godina.

SELECT fname, age  
FROM characters  
WHERE age BETWEEN 50 AND 100;

6. Ispišite godine svih likova tako da među njima nema onih sa istim godinama.  
   SELECT DISTINCT age  
   FROM characters;  
     
     
     
7. Ispišite sve informacije o likovima čiji je faculty \= Gryffindor i čije su godine preko 30\.  
   SELECT \*  
   FROM characters  
   WHERE faculty \= 'Gryffindor' AND age \> 30;  
8. Ispišite imena prva tri fakulteta iz tabele tako da se fakulteti ne ponavljaju.

SELECT DISTINCT faculty  
FROM characters  
LIMIT 3;

9. Ispišite imena likova čije ime počinje sa 'N' i ima 5 slova, ili čije ime počinje sa 'L'.  
   SELECT fname  
   FROM characters  
   WHERE  
   fname LIKE 'N\_\_\_\_' OR fname LIKE 'L%';  
10. Izračunajte prosečne godine svih likova.  
    SELECT AVG(age)   
    FROM characters   
11. Obrišite lika sa ID \= 11\.  
    DELETE FROM characters   
    WHERE char\_id \= 11;  
12. Ispišite prezime svih likova koja sadrže slovo 'a'.

SELECT lname  
FROM characters  
WHERE lname LIKE '%a%';

13. Koristite pseudonim da privremeno zamenite naziv kolone fname u Half-Blood Prince za stvarnog princa-polukrvnog.  
    SELECT fname AS \`Half-Blood Prince\`   
    FROM characters;  
      
14. Ispišite id i imena svih patronusa po abecednom redu, pod uslovom da su poznati.  
    SELECT char\_id, patronus  
    FROM characters  
    WHERE patronus IS NOT NULL AND  patronus \!='Unknown'  
    ORDER BY patronus;  
15. Koristite operator IN, ispišite ime i prezime likova čije je prezime Crabbe, Granger ili Diggory.  
    SELECT fname, lname  
    FROM characters  
    WHERE lname IN ('Crabbe', 'Granger', 'Diggory');  
16. Ispišite minimalne godine likova.

SELECT MIN(age)  
FROM characters 

17. Koristite operator UNION, ispišite imena iz tabele characters i naslove knjiga iz tabele library.  
    SELECT fname AS name  
    FROM characters  
    UNION ALL  
    SELECT book\_name AS name  
    FROM library;  
18. Koristite operator HAVING, izračunajte broj likova po svakom fakultetu, ostavljajući samo one fakultete gde je broj studenata veći od 1\.

SELECT faculty, COUNT(\*)  
FROM characters  
GROUP BY faculty  
HAVING COUNT(\*) \> 1;

