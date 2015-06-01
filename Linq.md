# Npoco LINQ

## Query

### Simple query

```csharp
var users = Database.Query<User>().Where(y => y.UserId == 2 && !y.IsMale).ToList();
```

### Advnaced Query

```csharp
var users = Database.Query<User>()
					.Where(y => y.UserId > 0)
					.OrderBy(x => x.Age)
					.ThenBy(x => x.Name)
					.Limit(50)
					.ToList();
```

# Delete

```csharp
Database.DeleteMany<User>().Where(x => x.IsMale == true).Execute();
```

