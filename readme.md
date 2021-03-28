### When we have this scenario

* Project **A**
* Project **B** : References Project **A**
* Project **C**: References Project **B**, and can not reference project **A**
* Project **B** have a class **XB**, that contains a field of type **XA** from **A**
* Project **B** have the next extension methods in class **XBAEx**
    *  For that field of type from **A**: means **XA**
    * Another Extension method with the same name, but for the Container `class` **XB** of the field **XA** which type is from **A**

now, if we tried to use the extension method of a class **XBAEx** from **B** inside the class **XC** of **C**, we can not compile the application
because the compiler will ask us, to reference **A** in **C**, but we did not use anything related to **A**.

#### But if we just changed the name of any one from the two extension methods, the error will gone.