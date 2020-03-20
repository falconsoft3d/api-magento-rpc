# Listar totas las ordenes de ventas de Magento
```
# -- coding: utf-8 --
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

# Version de Magento
```
magento = proxy.call(session, 'magento.info')
print(magento)
```

# Listar una Tienda especifica
```
args =  [{'store_id':'1'}]
store = proxy.call(session, 'core_store.list', args)
print(store)
```

# Listar Productos con PPRINT
```
import pprint
args =  []
product = proxy.call(session, 'catalog_product.list', args)
pprint.pprint(product)
```

