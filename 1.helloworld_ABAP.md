# ABAP Class Explanation

## **Hello World Code**

```abap
CLASS zcl_am_helloworld DEFINITION
  PUBLIC
  FINAL
  CREATE PUBLIC .

  PUBLIC SECTION.
  INTERFACES IF_OO_ADT_CLASSRUN.
  PROTECTED SECTION.
  PRIVATE SECTION.
ENDCLASS.



CLASS zcl_am_helloworld IMPLEMENTATION.

METHOD if_oo_adt_classrun~main.
    out->write( 'hello world' ).
ENDMETHOD.

ENDCLASS.
```

## **Class Definition Section**

```abap
CLASS zcl_am_helloworld DEFINITION
  PUBLIC
  FINAL
  CREATE PUBLIC .
```

- `CLASS zcl_am_helloworld DEFINITION`: Defines a global class named `ZCL_AM_HELLOWORLD`.
- `PUBLIC`: The class is accessible from other programs.
- `FINAL`: The class cannot be inherited by other classes.
- `CREATE PUBLIC`: Allows instances of this class to be created publicly using `CREATE OBJECT`.

---

## **Public Section**

```abap
  PUBLIC SECTION.
  INTERFACES IF_OO_ADT_CLASSRUN.
```

- `PUBLIC SECTION`: Defines attributes and methods that can be accessed outside the class.
- `INTERFACES IF_OO_ADT_CLASSRUN`: Implements the interface `IF_OO_ADT_CLASSRUN`, which is required to execute the program in the ABAP Development Tools (ADT).

---

## **Protected & Private Sections**

```abap
  PROTECTED SECTION.
  PRIVATE SECTION.
```

- `PROTECTED SECTION`: Attributes and methods in this section can only be accessed within the class and its subclasses.
- `PRIVATE SECTION`: Attributes and methods in this section can only be accessed within the class itself.

---

## **Class Implementation Section**

```abap
CLASS zcl_am_helloworld IMPLEMENTATION.
```

- Begins the implementation of the class.

---

## **Method Implementation**

```abap
METHOD if_oo_adt_classrun~main.
    out->write( 'hello world' ).
ENDMETHOD.
```

- `METHOD if_oo_adt_classrun~main`: Implements the `MAIN` method of the `IF_OO_ADT_CLASSRUN` interface.
- `out->write( 'hello world' )`:
  - `out` is an implicit output stream available in `IF_OO_ADT_CLASSRUN`.
  - `write( 'hello world' )` prints the text "Hello World" in the ADT console.

---

## **End of Class Implementation**

```abap
ENDCLASS.
```

- Marks the end of the class implementation.

---
