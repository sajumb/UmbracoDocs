---
title: TaxSource
description: API reference for TaxSource in Umbraco Commerce
---
## TaxSource

```csharp
public class TaxSource : ValueObjectBase
```

**Inheritance**

* Class [ValueObjectBase](../../umbraco-commerce-common/umbraco-commerce-common-models/valueobjectbase.md)

**Namespace**
* [Umbraco.Commerce.Core.Models](README.md)

### Constructors

#### TaxSource

```csharp
public TaxSource(Guid countryId, Guid? regionId = default(Guid?))
```


### Properties

#### CountryId

```csharp
public Guid CountryId { get; }
```


---

#### RegionId

```csharp
public Guid? RegionId { get; }
```


### Methods

#### DeepClone

```csharp
public override object DeepClone()
```


<!-- DO NOT EDIT: generated by xmldocmd for Umbraco.Commerce.Core.dll -->