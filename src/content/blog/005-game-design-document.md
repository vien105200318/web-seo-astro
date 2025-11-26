---
title: "Game Design Document - Biến Ý Tưởng Thành Hệ Thống"
description: "Xây dựng GDD chi tiết: mechanics, systems, và core gameplay loop"
pubDate: 2024-01-22
tags: ["game design", "GDD", "mechanics"]
image: "/images/blog/005-cover.jpg"
---

# Game Design Document

## Tại Sao Cần GDD?

Làm solo dev không có nghĩa là làm lung tung. Tôi cần một bản plan rõ ràng, nếu không sẽ lạc mất giữa đường.

## Core Gameplay Loop

```
Khám phá làng → Thu thập manh mối → Tương tác với linh hồn →
Giải puzzle dựa trên văn hóa dân gian → Tiến triển story →
Unlock khu vực mới → Repeat
```

## Main Mechanics

### 1. Exploration (Khám Phá)
- **First-person perspective**: Tăng immersion
- **Limited visibility**: Sương mù, đèn dầu tầm ngắn
- **Environmental storytelling**: Quan sát để hiểu câu chuyện
- **Hidden paths**: Phát hiện lối đi bí mật qua manh mối

### 2. Investigation (Điều Tra)
- **Photo mode**: Chụp ảnh bằng máy ảnh film cũ
- **Journal system**: Ghi chép suy luận
- **Item examination**: Xem kỹ vật phẩm, đọc thông tin
- **Dialogue**: Hỏi han NPC, ghi nhớ thông tin

### 3. Ritual System (Nghi Lễ)
**ĐÂY LÀ CORE MECHANIC ĐỘC ĐÁO**

Player phải thực hiện các nghi lễ dân gian:
- **Cúng cô hồn**: Đặt đúng vật phẩm, đúng vị trí, đúng giờ
- **Đốt vàng mã**: Mini-game fold giấy
- **Thắp hương**: Số lượng, vị trí quan trọng
- **Niệm chú**: Rhythm-based input

**Sai có thể attract aggressive spirits!**

### 4. Spirit Interaction (Tương Tác Linh Hồn)
- **Peaceful spirits**: Cho quest, thông tin
- **Aggressive spirits**: Phải pacify hoặc tránh
- **Detection**: Linh hồn phát hiện qua ánh sáng, tiếng động, thời gian

### 5. Stealth & Evasion
Không có combat! Player yếu thế:
- **Hide**: Trốn trong tủ, gầm giường, sau bàn thờ
- **Distraction**: Ném vật, tạo tiếng động
- **Prayer beads**: Limited use, tạm thời repel spirits
- **Holding breath**: Khi spirit ở gần

## Progression Systems

### Character
- **No levels**: Progression qua story và items
- **Stamina bar**: Chạy, crouch, hold breath
- **Sanity meter**: Gặp nhiều ma → mất sanity → hallucinations

### Items
- **Hương (Incense)**: Repel yếu spirits
- **Phù (Talisman)**: Bảo vệ tạm thời
- **Đèn lồng**: Light source, consumption-based
- **Máy ảnh**: Capture evidence
- **Chuỗi hạt**: Prayer beads, limited charges

## Game Structure

**5 Nights System** (inspired by FNAF but different)
- Mỗi night = 1 chapter story
- Thời gian real-time: 23h → 1h (10 phút gameplay)
- Objective mỗi đêm khác nhau
- Survival ít quan trọng hơn completing rituals

## Technical Specs

- **Engine**: Unity (quyết định sau khi cân nhắc UE5)
- **Graphics**: Low-poly nhưng atmospheric
- **Audio**: Binaural 3D sound (CỰC QUAN TRỌNG!)
- **Platform**: PC first, có thể port console sau

## Risks & Concerns

❌ **Ritual mechanics có quá phức tạp không?**
❌ **Player nước ngoài có hiểu văn hóa Việt?**
❌ **Scope quá lớn cho solo dev?**

GDD đã xong 70 trang. Tôi tự hào nhưng cũng... sợ. **Liệu tôi có thể biến nó thành hiện thực?**
