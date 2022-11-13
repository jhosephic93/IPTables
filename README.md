# IPTables

## Tablas

- **filter** Cortafuegos. Tabla por defecto
- **nat** Para hacer NAT
- **mangle** Marcar y modificar paquetes
- **raw** Depurar seguimiento conexión
- **security** Usada para MAC (SELinux)

## Tipo de tráfico y flujo

- Paquete del exterior con destino el equipo:
    - POSTROUTING de nat e INPUT de filter
- Paquete originado en el equipo que sale
    - OUTPUT de nat, OUTPUT de filter y POSTROUTING de nat.
- Paquete que atraviesa el equipo
    - PREROUTING de nat, FORWARD de filter y POSTROUTING de nat.

![](./img/iptables_filter_nat2.png)