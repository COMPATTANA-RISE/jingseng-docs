# รูปแบบข้อมูล

### Request Data

รูปแบบการส่งข้อมูลจาก Frontend -> Backend

- รูปแบบเป็น CamelCase (Ex. createdAt, updatedAt)
- Content Type `form-data | x-www-form-urlendcoded | application/json`
- Method `GET | POST | PUT | PATCH | DELETE`
- กรณีแนบไฟล์ `enctype="multipart/form-data"`

ตัวอย่าง

```json
{
  "username": "<username>",
  "email": "<email>",
  "password": "<password>",
  "isActive": true,
  "userDetail": {
    "firstname": "<firstname>",
    "lastname": "<lastname>",
    "phone": "<phone>",
    "address": "<address>",
    "birthdate": "<birthdate>"
  }
}
```

---

### Response Data

โครงสร้างการส่งข้อมูลกลับจาก Backend -> Frontend

- `success` ประเภท `boolean` : สถานะของการตอบกลับ `true | false`
- `statusCode` ประเภท `number` : สถานะของการตอบกลับ ดูในเอกสาร `การจัดการข้อผิดพลาด`
- `message` ประเภท `string` : ข้อความตอบกลับจาก Backend
- `data` ประเภท `Object | Array` : ข้อมูลที่ส่งให้ Frontend
- `errors` ประเภท `Array -> Object` : รายการข้อผิดพลาดที่เกิดขึ้น เป็น Array ที่มี Object Error พร้อมคำอธิบาย
- `paginate` ประเภท `Object` : ข้อมูลการแบ่งหน้าของข้อมูล

ตัวอย่าง

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Users fetched successfully",
  "data": [
    {
      "id": "ec286a99-9742-436f-97b9-0d578237e2ce",
      "username": "superadmin",
      "email": "superadmin@superadmin.com",
      "isActive": true,
      "companyId": null,
      "createdAt": "2025-07-02T07:54:10.869Z",
      "updatedAt": "2025-07-02T07:54:10.869Z",
      "roles": [
        {
          "id": "c8e4a596-eedb-4929-b6b7-d4c506774f83",
          "name": "superadmin",
          "description": "Super Admin"
        }
      ]
    },
    {
      "id": "7597d2dc-27f0-43b3-bfc4-bdb58a75e533",
      "username": "admin",
      "email": "admin@admin.com",
      "isActive": true,
      "companyId": null,
      "createdAt": "2025-07-02T07:54:10.935Z",
      "updatedAt": "2025-07-02T07:54:10.935Z",
      "roles": []
    },
    {...}
  ],
  "error": null,
  "paginate": {
    "limit": 2, // Int จำนวนต่อหน้า
    "page": 1, // Int หน้าปัจจุบัน
    "pages": 2, // Int หน้าทั้งหมด
    "total": 4, // Int จำนวนแถวข้อมูลทั้งหมด
    "nextUrl": "?page=2", // String
    "prevUrl": null // String
  }
}
```
