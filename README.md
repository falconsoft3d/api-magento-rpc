# Conectarse Python3
```
import xmlrpc.client
url = 'http://134.122.75.12:80'
username = 'odoo'
password = 'aqui_pones_pass'

proxy = xmlrpc.client.ServerProxy('{}/api/xmlrpc/'.format(url))
session = proxy.login('odoo', 'x1234567890')

args =  []
sales = proxy.call(session, 'sales_order.list', args)
print(sales)
```

