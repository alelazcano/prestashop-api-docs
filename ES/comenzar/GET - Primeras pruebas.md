Primeras pruebas

Cuando comienzas a usar el API Webservice de PRestashop, es importante validar que funcione tu credencial / token, además de confirmar que tienes los permisos suficientes.

Si estás comenzando un desarrollo, siempre recomiendo tener una instalación de Prestashop como sandbox o entorno de pruebas, donde dejes configurados datos de ejemplo (dummy) para testear a medida que avances. Luego tendrás un poco más claro qué necesitas para así desarrollar a tu cliente, avanzar con la integración y escribir código con más comodidad.

A mí siempre me gusta iniciar en el navegador completando http://demopresta.local/api?output_format=JSON y teniendo una extensión que convierta el JSON RAW (crudo) en una visualización amigable. Puedes probar [Json Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa) o [Json Viewer](https://chrome.google.com/webstore/detail/json-viewer/gbmdgpbipfallnflgajpaliibnhdgobh).

Primer GET con la API de Pestashop:

[*] en mi caso utilizo una instalación en localhost con el dominio `demopresta.local` para más facilidad.

Ejemplo de permisos 100% para todos los métodos y entidades/módulos:

```json
[
  "addresses",
  "attachments",
  "carriers",
  "cart_rules",
  "carts",
  "categories",
  "combinations",
  "configurations",
  "contacts",
  "content_management_system",
  "countries",
  "currencies",
  "customer_messages",
  "customer_threads",
  "customers",
  "customizations",
  "deliveries",
  "employees",
  "groups",
  "guests",
  "image_types",
  "images",
  "languages",
  "manufacturers",
  "messages",
  "order_carriers",
  "order_cart_rules",
  "order_details",
  "order_histories",
  "order_invoices",
  "order_payments",
  "order_slip",
  "order_states",
  "orders",
  "price_ranges",
  "product_customization_fields",
  "product_feature_values",
  "product_features",
  "product_option_values",
  "product_options",
  "product_suppliers",
  "products",
  "search",
  "shop_groups",
  "shop_urls",
  "shops",
  "specific_price_rules",
  "specific_prices",
  "states",
  "stock_availables",
  "stock_movement_reasons",
  "stock_movements",
  "stocks",
  "stores",
  "suppliers",
  "supply_order_details",
  "supply_order_histories",
  "supply_order_receipt_histories",
  "supply_order_states",
  "supply_orders",
  "tags",
  "tax_rule_groups",
  "tax_rules",
  "taxes",
  "translated_configurations",
  "warehouse_product_locations",
  "warehouses",
  "weight_ranges",
  "zones"
]```

Ejemplo de sólo acceso a algunas entidades, por ejemplo una integración logística, donde sólo daremos acceso un poco más restringido a:

```json
[
    "addresses",
    "contacts",
    "customers",
    "deliveries",
    "order_carriers",
    "order_states",
    "orders",
    "shops",
    "stores",
    "zones"
]```