1. Quản lý resource :  
- Thêm mới :  
```
pcs resource create	resource_id(name) standard:provider:type|type [resource options]
```
- Ví dụ :  
```
  pcs resource create Virtual_IP ocf:heartbeat:IPaddr2 ip=172.16.69.254 cidr_netmask=24 op monitor interval=30s
```
> Lưu ý :  
>- pcs resource create: yêu cầu gọi chức năng của câu lệnh
>- Virtual_IP: tên của resource hay resource_id
>  - ocf:heartbeat:IPaddr2: khai báo kiểu resource agent.
>  - ip=172.16.69.254, cidr_netmask=24: các giá trị của resource.
>  - op monitor interval=30s: Khai báo các tùy chọn cho resource.

- Xóa resource :  
```
 pcs resource delete resource_id
```  

- Liệt kê :  
```
  pcs resource list
```
