# IMU TPS Test - Programming Test Submission

A third-person shooter built in Unreal Engine 5.3 featuring stamina-based combat mechanics and interactive environmental zones.

## 🎮 Game Features

### Core Mechanics
- **Stamina-based damage system** replacing traditional health
- **Two weapon types** with distinct characteristics:
  - **Rifle**: 15 damage, 30 rounds, 4 shots/sec
  - **Pistol**: 5 damage + 20 bleed effect, 12 rounds, 0.2 shots/sec
- **Mouse wheel weapon switching** with array wrapping
- **Infinite ammo reload system** with persistent per-weapon tracking

### Combat System
- **Line trace shooting** from camera with muzzle offset
- **Bleed mechanics**: Pistol applies 2 damage/sec for 10 seconds (timer resets on re-hit)
- **Movement speed scaling** based on stamina:
  - 100-50% stamina: 600 units/sec
  - 50-25% stamina: 450 units/sec
  - 25-0% stamina: 150 units/sec

### UI & Visual Feedback
- **Player HUD** with stamina bar, ammo counter, weapon name, and reload prompt
- **Enemy floating stamina bars** with color-coding and "current/max" format
- **Real-time updates** via event-driven architecture

### Interactive Zones
- **Heal Zone**: Restores +20 stamina/sec
- **Damage Zone**: Applies -10 stamina/sec
- **Multi-character support** with modular zone system

## 🏗️ Technical Architecture

### Component Structure
- **BPC_WeaponComponent**: Encapsulated weapon logic with event dispatchers
- **BP_BaseCharacter**: Core stamina system, movement modifiers, and damage handling
- **BP_PlayerCharacter**: Player-specific logic with weapon component and HUD integration
- **BP_Enemy**: AI with floating stamina bar widget component
- **BP_ModifierZone**: Reusable zone base class with timer-based area effects

### Data-Driven Design
- **F_WeaponConfig**: Weapon configuration structure
- **F_WeaponInstance**: Runtime weapon state
- **F_WeaponState**: Current weapon properties
- **Data Assets**: DA_Rifle and DA_Pistol for weapon configurations

## 🎯 Controls

- **WASD**: Movement
- **Mouse**: Look around
- **Left Click**: Fire weapon
- **Mouse Wheel**: Switch weapons
- **R**: Reload (when out of ammo)
- **Space**: Jump

## 🚀 How to Run

### Option 1: Download Executable (Recommended)
1. Go to [Releases](https://github.com/noahbutcher97/IMU_TPS_Test/releases)
2. Download the latest build
3. Extract and run `IMU_TPS_Test.exe`

### Option 2: Build from Source
1. Clone this repository with Git LFS enabled
2. Open `IMU_TPS_Test.uproject` in Unreal Engine 5.3
3. Build and run from the editor

## 📋 Testing Checklist

All core requirements have been verified:
- ✅ Movement and camera controls
- ✅ Weapon switching and firing mechanics
- ✅ Damage application and bleed effects
- ✅ Stamina system and movement speed modifiers
- ✅ HUD updates and user feedback
- ✅ Interactive zone functionality
- ✅ Multi-character zone support

## 🛠️ Built With

- **Unreal Engine 5.3**
- **Blueprint Visual Scripting**
- **Git LFS** for asset management
- **Modular component architecture**

---

**Project Status**: Complete and ready for submission
**Engine Version**: Unreal Engine 5.3
**Platform**: Windows 64-bit
