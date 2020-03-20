# Conectarse Python3
```
import xmlrpc.client
url = 'http://134.122.75.77:80'
username = 'odoo'
password = 'x1234567890'

proxy = xmlrpc.client.ServerProxy('{}/api/xmlrpc/'.format(url))
session = proxy.login('odoo', 'x1234567890')

args =  []
sales = proxy.call(session, 'sales_order.list', args)
print(sales)
```

