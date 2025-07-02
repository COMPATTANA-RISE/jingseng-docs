# รหัสข้อผิดพลาด

## Http Status Code

### 2xx Success

- **200 OK** - คำขอสำเร็จ
- **201 Created** - สร้างทรัพยากรใหม่สำเร็จ
- **202 Accepted** - คำขอได้รับการยอมรับแต่ยังไม่ประมวลผลเสร็จ
- **204 No Content** - คำขอสำเร็จแต่ไม่มีเนื้อหาส่งกลับ

### 3xx Redirection

- **301 Moved Permanently** - ย้ายถาวร
- **302 Found** - พบทรัพยากรที่ย้ายไป
- **304 Not Modified** - ไม่มีการเปลี่ยนแปลง
- **307 Temporary Redirect** - ย้ายชั่วคราว

### 4xx Client Errors

- **400 Bad Request** - คำขอไม่ถูกต้อง
- **401 Unauthorized** - ไม่ได้รับอนุญาต (ต้อง login)
- **403 Forbidden** - ไม่อนุญาต (มีสิทธิ์ไม่เพียงพอ)
- **404 Not Found** - ไม่พบทรัพยากร
- **405 Method Not Allowed** - ไม่อนุญาต HTTP method นี้
- **406 Not Acceptable** - ไม่สามารถตอบสนองตามที่ client ต้องการ
- **409 Conflict** - ขัดแย้งกับข้อมูลที่มีอยู่
- **422 Unprocessable Entity** - ข้อมูลไม่ถูกต้อง (validation error)
- **429 Too Many Requests** - ส่งคำขอมากเกินไป
- **451 Unavailable For Legal Reasons** - ไม่สามารถเข้าถึงได้เนื่องจากเหตุผลทางกฎหมาย

### 5xx Server Errors

- **500 Internal Server Error** - ข้อผิดพลาดภายในเซิร์ฟเวอร์
- **501 Not Implemented** - ฟีเจอร์ยังไม่ได้ถูก implement
- **502 Bad Gateway** - ข้อผิดพลาดจาก gateway
- **503 Service Unavailable** - บริการไม่พร้อมใช้งาน
- **504 Gateway Timeout** - Gateway timeout
- **507 Insufficient Storage** - พื้นที่จัดเก็บไม่เพียงพอ
