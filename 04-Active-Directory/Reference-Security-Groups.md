# Security Group Reference Table

The table below maps the user accounts to their respective Active Directory security groups based on department, role, names:

| Department / Role | Security Group | Logon Name | Member Name | Account Type |
|-------------------|-----------------------|------------|-------------|--------------|
| **Administration** | `Administration-Sec-Group` | `corp\m.brown` <br> `corp\a.jones` | Michael Brown <br> Anna Jones | Standard <br> Standard |
| **Customer Service** | `Customer-Service-Sec-Group` | `corp\j.wilson` <br> `corp\s.miller` | James Wilson <br> Sarah Miller | Standard <br> Standard |
| **Finance** | `Finance-Sec-Group` | `corp\d.clark` <br> `corp\l.white` | David Clark <br> Laura White | Standard <br> Standard |
| **HR Department** | `HR-Sec-Group` | `corp\r.taylor` <br> `corp\e.davis` | Robert Taylor <br> Emma Davis | Standard <br> Standard |
| **IT Department (All)** | `IT-Sec-Group` | `corp\d.moore` <br> `corp\da.mooree` <br> `corp\s.hall` <br> `corp\so.hall` | Daniel Moore <br> Daniel Moore <br> Sophie Hall <br> Sophie Hall | Admin <br> Standard <br> Admin <br> Standard |
| **IT Admin** | `IT-Admin-Sec-Group` | `corp\d.moore` <br> `corp\s.hall` | Daniel Moore <br> Sophie Hall | Admin (System Administrator) <br> Admin (System Administrator) |
| **IT Standard** | `IT-Standard-Sec-Group` | `corp\da.mooree` <br> `corp\so.hall` | Sophie Hall | Standard (IT Support) <br> Standard |
