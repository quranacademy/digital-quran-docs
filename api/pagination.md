# Pagination

Some endpoints that return collections are paginated. For these endpoints, the `meta.pagination` object will tell you the current page, amount per page, total number of pages, and total count of the collection.

By default, the API will return the first page of results. Each page contains a maximum of 100 items, unless otherwise noted below. To fetch a particular page, use the `page` query parameter.

You can specify `per_page` parameter to set the amount of images to return. It must be an integer from 1 to the maximum number of items for a given action.

An example `meta.pagination` payload:

```javascript
{
    "data": [...],
    "meta": {
        "pagination": {
            "page": 1,
            "count": 100,
            "total_pages": 3,
            "total_count": 300
        }
    }
}
```

Note: `meta.pagination.count` is not equal to `per_page` parameter, it may be less on the last page.

