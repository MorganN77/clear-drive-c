# วิธีเคลียร์พื้นที่ไดรฟ์ C อย่างปลอดภัย (Windows)

## ✅ 1. ลบไฟล์ชั่วคราว
- เปิด Run (Win + R) แล้วพิมพ์ `temp` → ลบทั้งหมด
- เปิด Run แล้วพิมพ์ `%temp%` → ลบทั้งหมด

## ✅ 2. ใช้ Disk Cleanup
- พิมพ์ `Disk Cleanup` ใน Start Menu
- เลือก Drive C > กด “Clean up system files”
- ติ๊ก:
  - Windows Update Cleanup
  - Previous Windows installations
  - Temporary files

## ✅ 3. ลบ Prefetch
- Run > พิมพ์ `prefetch` → ลบทั้งหมด

## ✅ 4. ลบ System Restore Point เก่า
- Control Panel > System > System Protection > Configure > Delete

## ✅ 5. ลบ Windows.old
- ใช้ Disk Cleanup แล้วติ๊ก “Previous Windows installations”

## ✅ 6. เคลียร์ Windows Update Cache

```cmd
net stop wuauserv
net stop bits
del /s /q /f %windir%\SoftwareDistribution\Download\*
net start bits
net start wuauserv
