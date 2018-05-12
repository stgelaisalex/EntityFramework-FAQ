# Entity Framework - Deferred Query

## Introduction

Deferred Query allows you to defer immediate query execution from a LINQ method, like First or Count, to allow others third party libraries to use their features like caching.

## Why Deferred Query?

### Common scenario:

 - Allow other third party libraries to use LINQ immediate method

## Google Related Searches

 - [Entity Framework Deferred Execution](https://www.google.com/search?q=entity+framework+deferred+execution)
 - [Entity Framework Deferred vs Immediate Query Execution](https://www.google.com/search?q=entity+framework+deferred+vs+immediate+query+execution)

## StackOverflow Related Questions

 - [Entity Framework flexible cache](https://stackoverflow.com/questions/38527253/entity-framework-flexible-cache)
 - [Entity Framework second level cache](https://stackoverflow.com/questions/35549009/entity-framework-second-level-cache)



```csharp
// using Z.EntityFramework.Plus; // Don't forget to include this.
var ctx = new EntitiesContext();

// The count is deferred and cached.
var count = ctx.Customers.DeferredCount().FromCache();
```

## Supported Libraries

|Library	|Type	|EF Version	|Support	|Doc	|Features|
|:----------|:----------|:----------|:----------|:----------|:----------|
|[Z.EntityFramework.Plus](/ef-plus)	|FREE	|EF5<br>EF6<br>EF Core|	< 1 Day	|Yes    |Audit<br>Batch Delete<br>Batch Update<br>Cache<br>Deferred Query<br>Filter<br>Future<br>Include Filter<br>Include Optimized|