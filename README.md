# ROM Porting Automation

Automated ColorOS/OOS vendor porting onto HyperOS base using GitHub Actions.

## Device Info

| | Target Device | Donor Device |
|---|---|---|
| **Name** | Poco Pad 5G | OnePlus 12R 5G |
| **Codename** | ruan | - |
| **CPU** | Snapdragon 7s Gen 2 (SM7435) | Snapdragon 8 Gen 2 |
| **Screen** | 12.1 inches | 6.78 inches |
| **Camera** | 8MP + 8MP | 16MP + 50MP |

## What This Does

1. Downloads HyperOS ROM (Poco Pad 5G) and ColorOS/OOS ROM (OnePlus 12R 5G)
2. Extracts vendor partitions from both ROMs
3. Ports ColorOS vendor files onto HyperOS base:
   - Copies `group` and `passwd` from donor vendor/etc
   - Adds OPLUS properties to ODM build.prop
4. Repacks vendor partition as EROFS
5. Creates flashable ZIP
6. Uploads to Gofile and returns download URL

## How to Use

### 1. Go to Actions tab → "Port ColorOS to HyperOS"
### 2. Click "Run workflow"
### 3. Enter ROM URLs (or use defaults)
### 4. Wait for completion (~60-90 minutes)
### 5. Check workflow logs for Gofile download URL

## ⚠️ WARNING

- **FLASH AT YOUR OWN RISK!**
- Always backup your current ROM before flashing
- You need an unlocked bootloader and custom recovery
