# Supermarket-POS-System
A simple POS system for a supermarket written in C++.

Here is a powerpoint presentation on the project:
[SUPERMARKET POS SYSTEM presentation.pptx](https://github.com/RamisaMaliat/Supermarket-POS-System/files/5241246/SUPERMARKET.POS.SYSTEM.presentation.pptx)

## How info are stored?
- "File Format.txt" contains the format of all the files that are used by the system to store information.
- To log in as an administrator,one has to provide correct user id and password of one of the valid administrators. 
These info can be found inside "administrator" folder where each file represents an administrator named
as his/her user id.Again,log in info for managers or cashiers can be found in files named as their user ids(employee ids)
inside "branch/[branch id of the manager]/employees/manager" or "branch/[branch id of the cashier]/employees/cashiers"
respectively.All these files mentioned above also contain personal info of these users in their respective files.
- Personal info of the employees that are not users of the system can be found in files named as their employee ids
inside "branch/[branch id of the employee]/employees".info of deleted employees can be found in files named as 
"D[Employee id].txt"(Ex: "DB1EMP17.txt") inside "DeletedEmployeesHistory" folder.
- Information of a branch can be found in file [Branch id].txt inside "branch/[Branch id]". 
- Information of a product can be found in file [Product id].txt inside "product" folder.The daily requirements
and available quantity of these products in a branch are stored in "products.txt" inside "branch/[branch id]".
- All the ids used in the system are generated automatically and cannot be changed. Format:
	- Id for products: "P"+[product number]" -> Ex: P5
	- Id for branches: "B"+[branch number] -> Ex: B2
	- Id for administrators: "A"+[administrator number] -> Ex: A1
	- Id for employees:
		- Id for managers: [branch id]+"EMP"+[employee number]+"M"+[manager number] -> Ex: B1EMP1M1
		- Id for cashiers: [branch id]+"EMP"+[employee number]+"C"+[cashier number] -> Ex: B1EMP4C2
		- Id for other employees: [branch id]+"EMP"+[employee number] -> Ex: B2EMP19
    
 "Total.txt" keeps track of the numbers required to assign ids.
