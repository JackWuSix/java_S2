dataSourceKey: defaultDS
destination: example
groupId: g1
outerAdapterKey: canal-es
concurrent: true
dbMapping:
  database: erp             # 你的数据库名
  table: "tabWebsite Item"  # 重点：表名有空格，必须加双引号
  index: website_item_index # ES 里的索引名，建议全小写，下划线连接
  type: _doc                # ES 8.x 固定为 _doc
  id: name                  # 重点：主键是 name 字段
  upsert: true
  # 重点：SQL 里的表名必须加反引号 ``，否则数据库会报错
  sql: "select * from `tabWebsite Item`"
  website_item.yml
