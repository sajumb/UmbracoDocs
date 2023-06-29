---
title: OrderHasPropertySpecification
description: API reference for OrderHasPropertySpecification in Umbraco Commerce
---
## OrderHasPropertySpecification

```csharp
public class OrderHasPropertySpecification : IQuerySpecification<OrderReadOnly>, 
    ISpecification<OrderReadOnly>
```

**Inheritance**

* interface [IQuerySpecification&lt;!0&gt;](../../umbraco-commerce-common/umbraco-commerce-common-specifications/iqueryspecification-1.md)
* interface [ISpecification&lt;!0&gt;](../../umbraco-commerce-common/umbraco-commerce-common-specifications/ispecification-1.md)

**Namespace**
* [Umbraco.Commerce.Core.Specifications.Order](README.md)

### Constructors

#### OrderHasPropertySpecification (1 of 2)

```csharp
public OrderHasPropertySpecification(string key, string value, StringComparisonType comparisonType)
```

---

#### OrderHasPropertySpecification (2 of 2)

```csharp
public OrderHasPropertySpecification(KeyValuePair<string, string> property, 
    StringComparisonType comparisonType)
```


### Properties

#### ComparisonType

```csharp
public StringComparisonType ComparisonType { get; }
```


---

#### Property

```csharp
public KeyValuePair<string, string> Property { get; }
```


### Methods

#### Accept

```csharp
public void Accept(IVisitor visitor)
```


---

#### IsSatisfiedBy

```csharp
public bool IsSatisfiedBy(OrderReadOnly item)
```


<!-- DO NOT EDIT: generated by xmldocmd for Umbraco.Commerce.Core.dll -->