cat <<EOF > website_item.yml
dataSourceKey: defaultDS
destination: example
groupId: g1
outerAdapterKey: canal-es
concurrent: true
dbMapping:
  database: erp
  table: "tabWebsite Item"
  index: website_item_index
  type: _doc
  id: name
  upsert: true
  sql: "SELECT * FROM \`tabWebsite Item\`"
EOF
