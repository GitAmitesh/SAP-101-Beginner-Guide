# SAP HANA ABAP - Class `zcl_amitesh_compute` Explanation

## Declaration + Initialization method

```abap
DATA number1 TYPE i.
number1 = -8.
```

## In-Line Declaration method

```abap
DATA(number3) = -12.
```

## **Source Code**

```abap

CLASS zcl_amitesh_compute IMPLEMENTATION.
METHOD if_oo_adt_classrun~main.
*----------------------------------------------*
*Declaration + Initialization method*
 DATA number1 TYPE i.
 DATA number2 TYPE i.
 DATA result1 TYPE p LENGTH 8 DECIMALS 2.

 number1 = -8.
 number2 = 3.
 result1 = number1 / number2.
 DATA(output1) = |{ number1 } / { number2 } = { result1 }|.
 out->write( output1 ).
*----------------------------------------------*

*----------------------------------------------*
*In-Line Declaration method*
 DATA(number3) = -12.
 DATA(number4) = 4.
 DATA(result2) = number3 / number4.
 DATA(output2) = |{ number3 } / { number4 } = { result2 }|.
 out->write( output2 ).
*----------------------------------------------*
ENDMETHOD.
ENDCLASS.
```

## **Note: Class Definition was explained previously in helloworl_ABAP.md file. Therefore will not be repeated further.**

## **Class Implementation**

```abap
CLASS zcl_amitesh_compute IMPLEMENTATION.
```

- Begins the implementation of the class.

---

## **Method Implementation**

```abap
METHOD if_oo_adt_classrun~main.
```

- **METHOD if_oo_adt_classrun~main** → Implements the `main` method of `IF_OO_ADT_CLASSRUN`.
- The `~` symbol indicates interface method implementation.

---

## **Variable Declarations**

```abap
DATA number1 TYPE i.
DATA number2 TYPE i.
DATA result TYPE p LENGTH 8 DECIMALS 2.
```

- **DATA** → Declares variables.
- **number1 TYPE i** → Integer variable.
- **number2 TYPE i** → Integer variable.
- **result TYPE p LENGTH 8 DECIMALS 2** → Packed number (`p` type) with:
  - `8` digits in total.
  - `2` decimal places.

---

## **Assigning Values**

```abap
number1 = -8.
number2 = 3.
```

- Assigns `-8` to `number1` and `3` to `number2`.

---

## **Performing Division**

```abap
result = number1 / number2.
```

- **Division operation**: The result is stored in `result` (preserves decimals).

---

## **Formatted String Output**

```abap
DATA(output) = |{ number1 } / { number2 } = { result }|.
```

- Uses **ABAP string templates** (`|...|`).
- `{ number1 }`, `{ number2 }`, `{ result }` → Placeholders for variable values.

  **Example Output:**

  ```
  -8 / 3 = -2.67
  ```

---

## **Displaying Output**

```abap
out->write( output ).
```

- `out->write( output )` → Writes result to the ADT console (Eclipse).

---

## **End of Method and Class**

```abap
ENDMETHOD.
ENDCLASS.
```

- Marks the **end of the method** and **class implementation**.

---
