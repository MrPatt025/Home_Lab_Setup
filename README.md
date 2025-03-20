# Home_Lab_Cybersecurity
Building a Home Lab for Network Security Testing
# Cybersecurity Home Lab - Week 1: Lab Setup & Network Configuration

## Overview
ในสัปดาห์แรกนี้ เราได้ตั้งค่าพื้นฐานของ Cybersecurity Home Lab โดยมุ่งเน้นการติดตั้งเครื่องมือและสร้างสภาพแวดล้อมสำหรับการทดลองด้านความปลอดภัยเครือข่าย

## Tasks Completed
- **ติดตั้ง VirtualBox:**  
  - ดาวน์โหลดและติดตั้ง VirtualBox เพื่อใช้เป็น Hypervisor สำหรับการสร้างเครื่องเสมือน
- **นำเข้า VM:**  
  - **Kali Linux:** นำเข้าไฟล์ `.ova` สำหรับ VirtualBox จากเว็บไซต์ [Kali Linux](https://www.kali.org/get-kali/)  
  - **Metasploitable 2:** ดาวน์โหลดและนำเข้าไฟล์ `.vmdk` สำหรับ VM จาก [Metasploitable 2](https://sourceforge.net/projects/metasploitable/)
- **ตั้งค่าเครือข่าย:**  
  - สร้าง NAT Network ใน VirtualBox ด้วยเครือข่าย `192.168.100.1.4`  
  - กำหนดให้เครื่องเสมือนทั้ง Kali Linux และ Metasploitable 2 ใช้งาน NAT Network เดียวกัน
- **ทดสอบการเชื่อมต่อ:**  
  - ตรวจสอบ IP ด้วย `ip addr show` บน Kali Linux  
  - ทดสอบการเชื่อมต่อระหว่างเครื่องด้วยคำสั่ง `ping` ไปยัง Metasploitable 2  
  - สแกนพอร์ตและบริการด้วย `nmap -sV -O` เพื่อยืนยันว่ามีพอร์ตที่เปิดและช่องโหว่ที่สามารถทดลองโจมตีได้
- **ทดสอบ SSH (Optional):**  
  - ทดสอบการเชื่อมต่อผ่าน SSH ไปยัง Metasploitable 2 เพื่อตรวจสอบการทำงานของบริการ

## Outcome
- VirtualBox และ VM ทั้งสองทำงานได้อย่างถูกต้อง
- เครื่องเสมือนทั้งสองได้รับ IP จากเครือข่าย `192.168.100.1.4` และสามารถสื่อสารกันได้
- ผลการสแกนด้วย Nmap แสดงให้เห็นบริการที่เปิดอยู่บน Metasploitable 2 ซึ่งพร้อมสำหรับการทดลองโจมตีในสัปดาห์ถัดไป


