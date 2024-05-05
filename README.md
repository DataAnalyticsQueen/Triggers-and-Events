# Triggers-and-Events---Triggers and events 

SELECT *
FROM employee_demographics

SELECT * 
FROM employee_salary;

DELIMETER $$
CREATE TRIGGER employee_insert 
BEFORE INSERT ON employee_salary 
FOR EACH ROW 
BEGIN 
INSERT INTO Employee_demographics (employee_id,first_name,last_name)
VALUES (NEW.employee_id,NEW.first_name,NEW.last_name)
END $$
DELIMETER;

INSERT INTO employee_salary(employee_id,first_name,last_name,occupation,
salary,dept_id)

VALUES (13,'Jean-Ralphio','Saperstein''Entertainment 7200 CEO',1000000,NULL

--EVENTS 

SELECT * 
FROM employee_demographics;

CREATE EVENT delete_retirees
ON SCHEDULE every 30 SECOND 
DO 
BEGIN 
DELETE 
SELECT *
FROM Employee_demographics 
WHERE age >= 60;


END$$
DELIMETER;

SHOW VARIABLES like 'event%';

