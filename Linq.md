# Npoco LINQ

## Query

### Simple query

```chsarp
var users = Database.Query<User>().Where(y => y.UserId == 2 && !y.IsMale).ToList();
```

### Advnaced Query

```chsarp
var users = Database.Query<User>()
					.Where(y => y.UserId > 0)
					.OrderBy(x => x.Age)
					.ThenBy(x => x.Name)
					.Limit(50)
					.ToList();
```

# Delete

```chsarp
Database.DeleteMany<User>().Where(x => x.IsMale == true).Execute();
```

