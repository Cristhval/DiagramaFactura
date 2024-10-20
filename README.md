# DiagramaFactura
Justificación y reflexión escrita.
El diagrama de clases presente se encuentra orientado a la gestión de pedidos, facturación y pagos de un restaurante. Se explicará la estructura del
diagrama, las clases, las relaciones utilizadas y métodos utilizados.

Clases, atributos y métodos.
1. Cliente: esta clase cuanta con los atributos nombre, dirección y correo electrónico, estos atributos como sus nombres indican tienen como
objetivo tener el nombre, la dirección y correo del cliente para realizar la facturación, además se hace uso de tres métodos para obtener el
correo electrónico, nombre y la dirección.
2. Pedido: esta clase cuenta con los atributos número de pedido, fecha, estos atributos están orientados a generar el pedido del cliente, sus
métodos se centran en agregar o quitar y mostrar lo pedido.
3. ItemPedido: esta clase esta centrada en la cantidad y el precio unitario de los productos además de obtener la descripción de los productos y
de actualizar la cantidad pedida como métodos.
4. Producto: esta clase tiene como atributos el nombre del producto, el precio, la descripción y el id del producto y sus métodos están
orientados a obtener el precio, actualizar el precio en caso de que sea necesario y obtener el nombre del producto.
5. ItemFactura: esta clase tiene como atributos el producto y subtotal y su método se centra en calcular el subtotal a pagar sin impuestos.
6. Factura: esta clase tiene como atributos numero de factura, monto total, impuestos, descuentos y sus métodos son calcular el total a pagar,
imprimir la factura, enviar la factura al correo electrónico y la de registrar el método de pago.
7. Promoción: esta clase tiene los atributos descripción de la promoción, el porcentaje de descuento y como método aplicar la promoción.
8. Método de pago: esta clase tiene como atributo el monto a pagado y como método la validación del pago, además está asociada a tres
subclases las cuales son:
- Pago con transferencia: tiene como atributos numero de transferencia y banco de origen.
- Pago con Efectivo: tiene como atributo el cambio.
- Pago con Tarjeta: tiene como atributos el número de tarjeta, el titular y vencimiento.
9. Historial de factura: esta clase tiene como atributo la lista de facturas y sus métodos son agregar factura, consultar factura por fecha,
consultar factura por cliente, consultar factura por monto.


Relaciones
- La relación entre cliente y pedido es de asociación por que refleja que el cliente puede tener de uno a muchos pedidos.
- La relación entre pedido y factura es de asociación y esta refleja que abra una factura por un pedido.
- La relación entre pedido e item pedido es de asociación en esta relación se muestra que de un pedido puede haber muchas cantidades que
se pueden pedir.
- La relación entre item pedido y producto es de asociación y refleja la cantidad que se pidió de un producto desde uno a muchos.
- La relación entre producto e item factura es de asociación y refleja los productos de uno a muchos para calcular el subtotal.
- La relación entre item factura y de factura es de composición porque la factura depende de los datos de item factura para poder llevar a
cabo su proceso.
- La relación entre factura y promoción es de asociación porque puede haber de 0 a muchas promociones.
- La relación entre factura y historial de facturas es de agregación porque la clase historial de facturas agrega varias facturas, pero las
facturas no dependen del historial para existir.
