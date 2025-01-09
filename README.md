# SQL-injection-on-Birth-Certificate-System

## SQL Injection Vulnerability Description

### 1. **Vulnerability in `searchdata` POST Variable**  
**Location**: Admin search page (`/admin/search.php`)  
**Description**:  
The `searchdata` POST variable is susceptible to SQL Injection. If user input is not properly sanitized or validated, an attacker can craft malicious SQL queries that manipulate the database. This could lead to unauthorized access, data retrieval, or even data manipulation.

### 2. **Vulnerability in `userid` GET Parameter**  
**Location**: Admin user applications page (`/admin/users-applications.php`)  
**Description**:  
The `userid` GET parameter allows potential SQL Injection attacks. If the parameter is directly incorporated into SQL queries without adequate sanitization or prepared statements, an attacker can exploit this vulnerability to access or modify sensitive information in the database.

### **Impact**  
Both vulnerabilities, if exploited, can result in:  
- Unauthorized access to sensitive information.  
- Modification or deletion of database records.  
- Escalation of privileges within the application.  
- Full compromise of the underlying database system.

### **Mitigation Steps**  
1. Use parameterized queries or prepared statements to handle database interactions.  
2. Sanitize and validate all user inputs, ensuring special characters are escaped or rejected.  
3. Implement proper access controls on sensitive pages like admin interfaces.  
4. Regularly test the application for SQL Injection vulnerabilities using automated tools or manual security audits.

### **Severity**  
High – SQL Injection vulnerabilities are critical security flaws that can lead to severe consequences if exploited.
