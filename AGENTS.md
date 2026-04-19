# AD SYSTEM — AI Ad Team

## Project Overview
ระบบ AI ที่สร้างโฆษณาระดับโลกโดยอัตโนมัติ
ลูกค้าบอกแค่ชื่อสินค้า ระบบสร้าง Output 4 อย่าง:
1. Script / บทพูด
2. Image Prompts
3. Video Prompts
4. Next Steps Checklist

## Tech Stack
- Language: Python 3.11+
- AI: Anthropic Claude API
- Architecture: Multi-Agent Pipeline

## Structure
agents/          ← Agent แต่ละตัวมี identity + knowledge
core/            ← KnowledgeManager, AgentRunner, Pipeline
shared_knowledge/ ← ความรู้ที่ทุก Agent ใช้ร่วมกัน
output/          ← ผลลัพธ์ที่สร้างออกมา

## Commands
pip install -r requirements.txt  ← ติดตั้ง
python main.py                   ← รันสร้างโฆษณา
python main.py teach             ← สอน Agent ใหม่

## Important
- ทุก Agent โหลด Knowledge จากไฟล์ .md
- เพิ่มความรู้ได้โดยเพิ่มไฟล์ .md ใน knowledge/ folder
- ไม่ต้องแก้โค้ดเมื่อเพิ่มความรู้ใหม่
