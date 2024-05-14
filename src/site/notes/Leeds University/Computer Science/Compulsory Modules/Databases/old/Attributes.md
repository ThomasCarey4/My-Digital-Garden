---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/databases/old/attributes/"}
---

- Property of an [[Leeds University/Computer Science/Compulsory Modules/Databases/old/Entity\|Entity]] or a relationship
- Attribute Domain
	- Set of allowable values for one or more attributes
	- e.g. Age, 1 to 150 years
- Example: Influencer [[Leeds University/Computer Science/Compulsory Modules/Databases/old/Entity\|Entity]] with attribute ID, firstName, middleName, lastName, DOB, contactNo, and deliveryAddress
![Attribute Table Example.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Databases/old/images/Attribute%20Table%20Example.png)
**Simple Attribute**: An attribute composed of a *single* component with an independent existence, e.g. *ID*
**Composite Attribute**: An attribute compTsed of *multiple* components, each with an independent existence, e.g. *deliveryAddress* can be subdivided into Street, City and Postcode
**Derived Attribute**: An attribute that represents a value that is a derivable from a value of a related attribute, or set of attributes, not necessarily in the same entity type. e.g. *age* can be calculated from *DOB*
