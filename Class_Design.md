# Interface `IStorage`
 `IStorage` cung cấp một tập hợp các phương thức cần thiết để lưu trữ, truy xuất, và quản lý dữ liệu trong hệ thống. Nó đảm bảo rằng tất cả các lớp triển khai sẽ thực hiện theo cùng một tiêu chuẩn.


## Các phương thức

### 1. `SaveData(data: object, key: string): bool`

### 2. `LoadData(key: string): object`

### 3. `DeleteData(key: string): bool`

### 4. `ListKeys(): List<string>`

## CLass Diagram
![markdown](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3XSOPEQLf1Qb9IQdAdW6b-GN9QQdAbHpAO11S69PgajYIQ96Ic99efL2Vb9MQdA9Za9sQgMLGd59KMPUkgQLGb9-VWvKlKz-OWfOFQeAY3we6fVKdDGIYAcupSaiBl5EhIpMqBG2isqWYkouQhcuk1nIyr9AStC00000__y30000)


---

# Lớp `Storage`

Lớp `Storage` là một triển khai cụ thể của giao diện `IStorage`, được thiết kế để thực hiện các chức năng lưu trữ dữ liệu vào một tệp cơ sở dữ liệu hoặc nơi lưu trữ được chỉ định.

## Thuộc tính

### 1. `DatabaseFile` (Private)
- **Kiểu dữ liệu:** `string`

---

## Các phương thức

### 1. `SaveData(data: object, key: string): bool`

### 2. `LoadData(key: string): object`

### 3. `DeleteData(key: string): bool`

### 4. `ListKeys(): List<string>`

## Class Diagram
![markdown](https://www.planttext.com/plantuml/png/TCuz2i9040NWVa_noWJq0ej5Yc2ZNKumIOQmEid2paG8uiaiF99NaFnOM3ZLmFlcCU_dgr2ZP6ClRfv6I1MLnKGTu-u0O8-IZ6fIFWPX3xKKXcw9W8fkFCTPIqOUiRvmOpjSUVh2tAEEKJP_ZjGk_bUiTvifMTZMrlyzGUt4asQvN_R3zjN3kOA7Tkpb0m00__y30000)
