# ระบบจัดการสต็อกสินค้า (Inventory Management System)

## 1. รายละเอียดโครงงาน

ระบบจัดการสต็อกสินค้าเป็นโปรแกรมที่พัฒนาด้วยภาษา Python ทำงานผ่าน Terminal โดยมีวัตถุประสงค์เพื่อช่วยจัดการข้อมูลสินค้าในคลังสินค้า เช่น การเพิ่มสินค้า การแสดงรายการสินค้า การปรับปรุงจำนวนสินค้า การค้นหาสินค้า การสรุปข้อมูลสต็อก และการลบสินค้า

## 2. ความสามารถของโปรแกรม

โปรแกรมมีความสามารถทั้งหมด 7 เมนู ดังนี้

1. **เพิ่มสินค้า (Add Product)**  
   เพิ่มสินค้าใหม่ โดยระบุรหัสสินค้า ชื่อสินค้า ราคา และจำนวนสินค้า

2. **แสดงรายการสินค้า (View Product)**  
   แสดงรายการสินค้าทั้งหมดที่มีอยู่ในระบบ

3. **ปรับปรุงสต็อกสินค้า (Update Stock)**  
   เพิ่มหรือลดจำนวนสินค้าที่มีอยู่ในคลัง

4. **ค้นหาสินค้า (Search Product)**  
   ค้นหาสินค้าจากรหัสสินค้าหรือชื่อสินค้า

5. **สรุปข้อมูลสต็อก (Stock Summary)**  
   คำนวณมูลค่าสินค้ารวม จำนวนสินค้าทั้งหมด และแจ้งเตือนเมื่อสินค้าเหลือน้อย

6. **ลบสินค้า (Remove Product)**  
   ลบสินค้าออกจากระบบโดยใช้รหัสสินค้า

7. **ออกจากโปรแกรม (Exit)**  
   สิ้นสุดการทำงานของโปรแกรม

## 3. เครื่องมือที่ใช้

- ภาษา Python 3
- โปรแกรม Visual Studio Code สำหรับเขียนและแก้ไขโค้ด
- Terminal สำหรับเรียกใช้งานโปรแกรม

โปรแกรมไม่จำเป็นต้องติดตั้งไลบรารีเพิ่มเติม

## 4. วิธีการใช้งานโปรแกรม

1. เปิด Terminal
2. เข้าไปยังโฟลเดอร์ที่เก็บไฟล์โปรแกรม
3. ใช้คำสั่งต่อไปนี้เพื่อเริ่มต้นโปรแกรม

```bash
python3 main.py หรือ ./main.py
```

4. เลือกเมนูที่ต้องการใช้งาน โดยพิมพ์หมายเลขตั้งแต่ 1 ถึง 7
5. ปฏิบัติตามคำแนะนำที่แสดงบนหน้าจอ

## 5. โครงสร้างข้อมูล

โปรแกรมใช้ **List และ Dictionary** ในการจัดเก็บข้อมูลสินค้า โดยสินค้าแต่ละรายการประกอบด้วยข้อมูล 4 ส่วน ได้แก่

- `id` รหัสสินค้า ใช้ระบุสินค้าแต่ละรายการ
- `name` ชื่อสินค้า
- `price` ราคาสินค้าต่อหน่วย
- `quantity` จำนวนสินค้าที่มีอยู่ในสต็อก

ตัวอย่างข้อมูลสินค้า

```python
{
    "id": "P001",
    "name": "Pen",
    "price": 10.0,
    "quantity": 5
}
```

## 6. การตรวจสอบความถูกต้องของข้อมูล

โปรแกรมมีการตรวจสอบข้อมูลก่อนดำเนินการ เพื่อช่วยลดข้อผิดพลาดในการใช้งาน เช่น

- ตรวจสอบรหัสสินค้าและชื่อสินค้าว่าต้องไม่เป็นค่าว่าง
- ตรวจสอบไม่ให้เพิ่มรหัสสินค้าที่ซ้ำกัน
- ตรวจสอบราคาและจำนวนสินค้าไม่ให้เป็นค่าติดลบ
- ตรวจสอบว่าราคาเป็นตัวเลขและจำนวนสินค้าเป็นจำนวนเต็ม
- ตรวจสอบตัวเลือกเมนูว่าถูกต้องหรือไม่
- ตรวจสอบจำนวนสินค้าคงเหลือก่อนลดสต็อก

## 7. ข้อจำกัดของโปรแกรม

- ข้อมูลสินค้าถูกจัดเก็บไว้ในหน่วยความจำระหว่างที่โปรแกรมทำงานเท่านั้น
- เมื่อปิดโปรแกรม ข้อมูลที่เพิ่มหรือแก้ไขระหว่างการใช้งานจะไม่ถูกบันทึกไว้
- โปรแกรมทำงานผ่าน Terminal และยังไม่มีส่วนติดต่อผู้ใช้แบบกราฟิก

## 8. สรุปโครงงาน

ระบบจัดการสต็อกสินค้าเป็นโปรแกรมที่ช่วยจัดการข้อมูลสินค้าในเบื้องต้น โดยประยุกต์ใช้ความรู้ภาษา Python ได้แก่ ตัวแปร เงื่อนไข การวนซ้ำ ฟังก์ชัน List Dictionary และการจัดการข้อผิดพลาด เพื่อให้สามารถจัดการสินค้าได้อย่างเป็นระบบและสะดวกต่อการใช้งาน

# Inventory Management System

## 1. Project Overview

The Inventory Management System is a Python-based application that runs via the Terminal. It is designed to assist in managing warehouse inventory, including adding products, viewing the product list, updating stock quantities, searching for items, generating stock summaries, and removing products.

## 2. Program Features

The program offers 7 distinct functions:

1. **Add Product**
Add a new item by specifying its product ID, name, price, and quantity.

2. **View Product**
Display a list of all products currently in the system.

3. **Update Stock**
Increase or decrease the quantity of items in the inventory.

4. **Search Product**
Find products by their ID or name.

5. **Stock Summary**
Calculate the total value of inventory, the total number of items, and receive alerts for low-stock products.

6. **Remove Product**
Delete an item from the system using its product ID.

7. **Exit**
Terminate the program.

## 3. Tools Used

- Python 3
- Visual Studio Code (for writing and editing code)
- Terminal (for running the program)

No additional libraries are required.

## 4. How to Use the Program

1. Open the Terminal.
2. Navigate to the folder containing the program file.
3. Run the following command to start the program:

```bash
python3 inventory.py
```

Note: If your Python file has a different name, replace `inventory.py` with the actual filename.

4. Select the desired option from the menu. by entering a number from 1 to 7.
5. Follow the instructions displayed on the screen.

## 5. Data Structure

The program uses **Lists and Dictionaries** to store product information. Each product entry consists of four components:

- `id`: A unique identifier for each product.
- `name`: The name of the product.
- `price`: The unit price of the product.
- `quantity`: The number of items currently in stock.

Example of product data:

```python
{
"id": "P001",
"name": "Pen",
"price": 10.0,
"quantity": 5
}
```

## 6. Data Validation

The program validates data before processing to minimize operational errors, such as:

- Ensuring that the product ID and name are not left blank.
- Preventing the addition of duplicate product IDs.
- Ensuring that the price and quantity are not negative values.
- Verifying that the price is a numeric value and the quantity is an integer.
- Checking that the selected menu option is valid.
- Verifying that sufficient stock is available before reducing the inventory.

## 7. Program Limitations

- Product data is stored only in the system's memory while the program is running.
- Once the program is closed, any data added or modified during the session will not be saved.
- The program operates via the terminal and does not currently feature a graphical user interface (GUI).

## 8. Project Summary

This inventory management system serves as a basic tool for handling product data. It applies core Python concepts—including variables, conditional statements, loops, functions, lists, dictionaries, and error handling—to enable systematic and convenient product management.