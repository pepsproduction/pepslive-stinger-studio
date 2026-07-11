# PepsLive Stinger Studio

เครื่องมือสร้าง OBS Stinger Transition แบบ static web สำหรับ PepsProduction / PepsLive

## เปิดใช้งาน

เปิดไฟล์ `index.html` ได้ทันที หรืออัปทั้งโฟลเดอร์ขึ้น GitHub Pages

```text
pepslive-stinger-studio/
  index.html
  assets/
    css/style.css
    js/app.js
    img/pepsproduction-logo.png
```

## ฟีเจอร์หลัก

- โลโก้ PepsProduction อยู่มุมบนซ้ายของเว็บ
- Preset curated 21 แบบ แยกแนว Live Sport, TV, Arena, Replay, Sponsor, Premium, Broadcast, 3D, Lightning, Fire, Water, Storm, Speed, Glitch, Shatter และ Liquid
- Canvas preview 16:9 พร้อม timeline scrubber
- Preview Quality แยกจาก Export Resolution เพื่อให้พรีวิวลื่น แต่ export ยังเต็มคุณภาพ
- ปุ่ม Loop Preview สำหรับวนดู transition ต่อเนื่องก่อน export
- ตั้งค่า duration, OBS transition point, FPS, resolution, bitrate
- Effect layers: curtain panels, fluid matte, soft ribbons, 3D depth, orbit camera, lightning, ember sparks, liquid wave, prism shards, cine zoom, RGB split, glitch flash, displacement pulse, shatter tiles, alpha sweep, shockwave, light rays, lens flare, glow mist, logo bloom, energy ring, chromatic edge, vignette, camera shake, motion blur
- Preset ใหม่ `Silk Matte` และ `Studio Bloom` เน้นภาพนุ่ม ลื่น และไม่เป็นเส้นแข็ง เหมาะกับงาน broadcast/premium
- Preset 3D ใหม่ `Orbit Depth` และ `Holo Cube` เพิ่มมิติแบบกล้องหมุน/ฉากลึกสำหรับ opener และ replay
- Preset โหดใหม่ `Storm Reactor`, `Pyro Forge`, `Tidal Forge`, `Prism Rift`, `Maelstrom Core` สำหรับสายฟ้า ประกายไฟ คลื่นน้ำ และ prism 3D
- Preset ตัดต่อสมัยใหม่เพิ่ม `Velocity Ramp`, `RGB Glitch Pro`, `Aether Shatter`, `Liquid Glass Zoom` ในสไตล์ speed ramp, glitch, shatter และ liquid glass โดยไม่ลอก template ของแอปอื่น
- องศาแสงปรับได้ครบ 0-360 องศา
- Export loop ใช้ frame index ตาม FPS เพื่อลดจังหวะสะดุดจากเครื่องตอนบันทึก
- ปุ่ม `วิธีใช้` รายหมวด พร้อม popup อธิบายการใช้งาน
- Auto White Matte สำหรับโลโก้ที่มีพื้นหลังขาว
- ดูดสีจากโลโก้เพื่อทำ palette
- Export เป็น `.webm` ด้วย MediaRecorder ทั้งแบบ Standard และ OBS Track Matte side-by-side
- Save/Load project เป็น JSON และ autosave ใน browser

## ค่า OBS แนะนำ

```text
Scene Transition: Stinger
Transition Point Type: Time (milliseconds)
Transition Point: ใช้ค่าที่แสดงในหน้าเว็บ
Video File: ไฟล์ .webm ที่ export
```

## แนวทางอัปเกรดต่อ

OBS Studio 27+ รองรับ Track Matte Stinger Transition ซึ่งใช้วิดีโอ mask ขาว/ดำ/เทาเพื่อคุมการเปลี่ยนจากซีนเดิมไปซีนใหม่ ทำให้ transition สามารถ reveal ภาพได้เนียนกว่าการใช้ cut point อย่างเดียว ในเวอร์ชันนี้เลือก `Export Mode > OBS Track Matte` เพื่อบันทึกไฟล์แบบ side-by-side ได้เลย โดยฝั่งซ้ายเป็นวิดีโอ stinger และฝั่งขวาเป็น luma matte สำหรับตั้งค่า Track Matte ใน OBS

## GitHub Pages

โปรเจกต์นี้เป็นเว็บแยกของตัวเอง ไม่ผูกกับ `PepsLive_Tournament_Studio`

ตั้งค่า GitHub Pages:

```text
Settings > Pages > Build and deployment
Source: Deploy from a branch
Branch: main
Folder: /root
```

หลังเปิด Pages แล้ว URL จะเป็น:

```text
https://pepsproduction.github.io/pepslive-stinger-studio/
```
