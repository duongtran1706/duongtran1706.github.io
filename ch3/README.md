# Cấu trúc hệ thống

```mermaid
graph TD;
    api-sidercar-->promotions-srv;
    api-sidercar-->application-srv;
    api-sidercar-->master-data;
    promotions-srv -->master-data;
    promotions-srv-->application-srv;
    master-data-->promotions-srv;
    caculate-srv-->master-data;
    ecomv2Promotions --> master-data;

```

* [promotions](./promotion/README.md)
* [master-data](./master-data//README.md)