up:: [[Data MOC]]
tags:: #Programming  
# XML (Exchange Markup Language)
- Akin to [[JSON]], used in [[FIX Protocol]] (FIXML)
```
<stock>
  <symbol>GOOG</symbol>
  <price>2725.60</price>
  <volume>1200000</volume>
</stock>

```

| Feature            | JSON                               | XML                                                        |
| ------------------ | ---------------------------------- | ---------------------------------------------------------- |
| **Syntax**         | Lightweight, minimal               | Verbose, tag-based                                         |
| **Data Types**     | Native (numbers, booleans, arrays) | All values are text unless parsed                          |
| **Readability**    | Easier for humans                  | Can be more cumbersome                                     |
| **Parsing**        | Faster in modern apps              | More overhead                                              |
| **Use Case Fit**   | APIs, web, config files            | Documents, complex data exchange (finance, legacy systems) |
| **Schema Support** | JSON Schema (optional)             | XML Schema (XSD) supports strong validation                |