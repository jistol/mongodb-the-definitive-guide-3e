## Attribute Pattern
```json
// other pattern
{
    title: "Star Wars",
    director: "George Lucas",
    ...
    release_US: ISODate("1977-05-20T01:00:00+01:00"),
    release_France: ISODate("1977-10-19T01:00:00+01:00"),
    release_Italy: ISODate("1977-10-20T01:00:00+01:00"),
    release_UK: ISODate("1977-12-27T01:00:00+01:00"),
    ...
}

// indexes for search by release
{release_US: 1}
{release_France: 1}
{release_Italy: 1}
...
```

```json
// attribute pattern
{
    title: "Star Wars",
    director: "George Lucas",
    ...
    releases: [
        {
        location: "USA",
        date: ISODate("1977-05-20T01:00:00+01:00")
        },
        {
        location: "France",
        date: ISODate("1977-10-19T01:00:00+01:00")
        },
        {
        location: "Italy",
        date: ISODate("1977-10-20T01:00:00+01:00")
        },
        {
        location: "UK",
        date: ISODate("1977-12-27T01:00:00+01:00")
        },
        ...
    ],
    ...
}

// indexes for search by release
{ "releases.location": 1, "releases.date": 1}
```



Reference : [Building with Patterns: The Attribute Pattern](https://www.mongodb.com/developer/how-to/attribute-pattern/) 
