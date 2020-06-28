
```sql

result = "TableName".select('').where('').joins('').order('').page(page || 1).per(per_page || 10)

# 总数
result.total_count
# 总页数
result.total_pages

```