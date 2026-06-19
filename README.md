# ⛪ Cerkov & Anjeli — XR Mobilná Hra

## 🎬 Demo video


|                                       |
| ------------------------------------- |
| ▶️ Kliknutím prehráte demo na YouTube |


---

## O Projekte

Tento projekt je **interaktívna XR (Extended Reality) mobilná hra** vytvorená v engine **Unity** v rámci predmetu **Systémy Virtuálnej Reality (SVR)**.

Hráč sa pohybuje vo vlastnom 3D svete s **kostolíkom (cerkov)** vymodelovaným v programe **SketchUp**. Keď hráč vojde do určenej zóny, **spustí sa udalosť** — z neba začnú **zostupovať anjeli** s mávajúcimi krídlami, ktorí po pristátí pokojne **levitujú** nad zemou.

### Cieľ Projektu

Hlavným cieľom projektu je:

- Vytvoriť **vlastný 3D svet** s objektom vymodelovaným v SketchUp
- Pridať **interaktívne prvky** a reakcie na pohyb hráča
- Implementovať **collision (kolíznu) interakciu**, ktorá slúži ako *trigger* (spúšťač) udalosti
- Využiť **vstavané XR nástroje Unity** na nasadenie aplikácie do mobilného telefónu (**iPhone**)
- Umožniť **plynulé ovládanie pohybu** dotykom na mobilnom zariadení

---

## ✨ Hlavné Prvky

- **Kostolík (Cerkov)** — vlastný 3D model vytvorený v SketchUp
- **Anjeli** — vymodelovaní v rovnakom štýle ako kostolík (krídla sú prevzaté), s **animáciou letu a levitácie**
- **Trigger zóna** — pri vstupe hráča do zóny sa spustí zostup anjelov (kolízna detekcia)
- **AR / XR režim** — aplikácia beží na iPhone s možnosťou zapnutia/vypnutia kamery (AR pozadie)
- **Mobilné ovládanie** — virtuálny joystick na pohyb + tlačidlo na šprint
- **Desktopové ovládanie (WASD)** — pomocné ovládanie pre testovanie na PC

---

## 🛠️ Použité Technológie

- **Unity** (Universal Render Pipeline — URP)
- **AR Foundation** — `ARCameraBackground`, XR Origin
- **XR Plugin Management** — nasadenie na mobil
- **SketchUp** — modelovanie kostolíka (`.skp`)
- **C#** — herná logika a skripty
- **Joystick Pack** — mobilné dotykové ovládanie
- **Fantasy Skybox** + **Terrain** — prostredie sveta

---

## 📦 Obsah Projektu

```
na odovzdanie/
├── XR_hra/                         # Unity projekt (XR hra)
│   ├── Assets/
│   │   ├── Scripts/                # Herné C# skripty
│   │   │   ├── AngelDescent.cs         # Zostup + levitácia + animácia krídel
│   │   │   ├── AngelTriggerZone.cs     # Kolízna trigger zóna
│   │   │   ├── JoystickMovement.cs     # Mobilný pohyb (joystick + šprint)
│   │   │   ├── DesktopWASDControls.cs  # Pomocné WASD ovládanie (PC)
│   │   │   └── ARCameraToggle.cs       # Prepínanie AR pozadia (On/Off)
│   │   ├── my_models/              # Vlastné modely (Cerkov.skp, anjel.fbx)
│   │   ├── Scenes/                 # Herná scéna (SampleScene.unity)
│   │   ├── Joystick Pack/          # Knižnica mobilného joysticku
│   │   └── Fantasy Skybox FREE/    # Skybox prostredia
│   ├── ProjectSettings/
│   └── Packages/
├── Cerkov17.skp                    # SketchUp model kostolíka
├── Anaglyf/                        # Anaglyfické 3D snímky (ďalšia úloha)
└── NeRF_Gaussian_Splatting_essay.docx  # Esej (ďalšia úloha)
```

---

## ▶️ Inštalácia a Spustenie

### Otvorenie projektu v Unity

1. Rozbaľte archív a otvorte priečinok `XR_hra` v **Unity Hub** (odporúčaná verzia podľa `ProjectSettings`).
2. Otvorte scénu `Assets/Scenes/SampleScene.unity`.
3. Stlačte **Play** pre spustenie v editore (na PC použite WASD ovládanie).

### Nasadenie na iPhone

1. V `Build Settings` zvoľte platformu **iOS**.
2. Skontrolujte nastavenia **XR Plug-in Management** a **AR Foundation**.
3. Vytvorte build a nasaďte projekt cez **Xcode** do zariadenia.

---

## 🎮 Návod na Používanie

### Na mobile (iPhone)

- **Ľavý joystick** — pohyb hráča vo svete
- **Tlačidlo Šprint** — zrýchlený pohyb
- **Tlačidlo AR On / AR Off** — zapnutie/vypnutie kamery (AR pozadia)
- **Príď ku kostolíku** — vstupom do trigger zóny privoláš zostup anjelov 👼

### Na PC (testovanie)

- **WASD / šípky** — pohyb
- **Myš** — otáčanie pohľadu
- **Shift** — šprint
- **ESC** — uvoľnenie kurzora

---

## 🔍 Ako Funguje Interakcia

1. Anjeli sú na začiatku **skrytí** (`AngelDescent` ich na štarte zneviditeľní).
2. Keď hráč vojde do kolíznej zóny, `AngelTriggerZone` zavolá `TriggerArrival()`.
3. Anjeli sa **zobrazia**, spustí sa **animácia letu krídel** a začnú **zostupovať** zhora nadol (plynulý `SmoothStep`).
4. Po pristátí anjeli **navždy levitujú** (jemný pohyb hore/dole pomocou sínusovej funkcie).

---

## 👤 Autor

**Jakub Filičko**

Predmet: Systémy Virtuálnej Reality (SVR)
Katedra počítačov a informatiky
Technická univerzita v Košiciach

---

  


# ⛪ Church & Angels — XR Mobile Game (English)

## About the Project

This project is an **interactive XR (Extended Reality) mobile game** built in the **Unity** engine for the **Virtual Reality Systems (SVR)** course.

The player walks through a custom 3D world featuring a **small church (cerkov)** modeled in **SketchUp**. When the player enters a designated zone, an **event is triggered** — **angels descend** from the sky with flapping wings and, once they land, calmly **levitate** above the ground.

### Project Goals

The main goals of the project are:

- Create a **custom 3D world** with an object modeled in SketchUp
- Add **interactive elements** that react to the player's movement
- Implement a **collision interaction** that acts as a *trigger* for an event
- Use Unity's **built-in XR tools** to deploy the app to a mobile phone (**iPhone**)
- Provide **smooth touch-based movement controls** on the mobile device

---

## ✨ Key Features

- **Church (Cerkov)** — custom 3D model created in SketchUp
- **Angels** — modeled in the same style as the church (wings are borrowed), with **flight and levitation animation**
- **Trigger zone** — entering the zone starts the angels' descent (collision detection)
- **AR / XR mode** — runs on iPhone with a toggle for the camera background (AR On/Off)
- **Mobile controls** — virtual joystick for movement + sprint button
- **Desktop controls (WASD)** — helper controls for testing on PC

---

## 🛠️ Tech Stack

- **Unity** (Universal Render Pipeline — URP)
- **AR Foundation** — `ARCameraBackground`, XR Origin
- **XR Plugin Management** — mobile deployment
- **SketchUp** — church modeling (`.skp`)
- **C#** — game logic and scripts
- **Joystick Pack** — mobile touch controls
- **Fantasy Skybox** + **Terrain** — world environment

---

## ▶️ Installation and Running

### Open the project in Unity

1. Extract the archive and open the `XR_hra` folder in **Unity Hub** (use the version recommended in `ProjectSettings`).
2. Open the scene `Assets/Scenes/SampleScene.unity`.
3. Press **Play** to run in the editor (use WASD controls on PC).

### Deploy to iPhone

1. In `Build Settings`, select the **iOS** platform.
2. Verify **XR Plug-in Management** and **AR Foundation** settings.
3. Build and deploy the project to the device via **Xcode**.

---

## 🎮 Quick User Guide

### On mobile (iPhone)

- **Left joystick** — move the player around the world
- **Sprint button** — faster movement
- **AR On / AR Off button** — toggle the camera (AR background)
- **Walk up to the church** — entering the trigger zone summons the descending angels 👼

### On PC (testing)

- **WASD / arrows** — movement
- **Mouse** — look around
- **Shift** — sprint
- **ESC** — release the cursor

---

## 🔍 How the Interaction Works

1. The angels are **hidden** at the start (`AngelDescent` makes them invisible on start).
2. When the player enters the collision zone, `AngelTriggerZone` calls `TriggerArrival()`.
3. The angels **appear**, the **wing flight animation** plays, and they begin to **descend** from above (smooth `SmoothStep` motion).
4. After landing, the angels **levitate forever** (gentle up/down motion via a sine function).

---

## 👤 Author

**Jakub Filičko**

Course: Virtual Reality Systems (SVR)
Department of Computers and Informatics
Technical University of Košice

---

**Verzia / Version**: 1.0