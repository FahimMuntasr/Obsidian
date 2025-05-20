
## 🔧 Arch Linux Maintenance Guide (Video Summary)

### **Introduction**

- The speaker emphasizes the importance of regular system maintenance on Arch Linux, especially due to its **rolling release nature**.
    
- Their personal experience: no crashes or issues thanks to consistent maintenance.
    
- Resources:
    
    - ArchWiki: System Maintenance
        
    - ArchWiki: Pacman Tips and Tricks
        

---

## 🛠️ Common Maintenance Tasks

### 1. **Check for Failed `systemd` Services**

- Command:
    
    ``systemctl --failed`
    
- Use when hardware or subsystems (e.g., Bluetooth, printers) malfunction.
### 2. **Inspect Logs with `journalctl`**

- Command:
    `sudo journalctl -p 3 -xb`
- View logs for **priority 3 (errors)** from the last boot.
- Useful for kernel errors, driver issues, etc.

### 3. **System Updates**

- Command:
    `sudo pacman -Syu`
- Frequency: **Daily or every 2 days.**
- Ensures stability in a rolling release system like Arch.
- For AUR users:
    `yay -Syu`
- `yay` updates both official and AUR packages.

---

## 🧹 Cache Management

### 4. **Clear Unused Package Cache**

- Removes cached packages **not currently installed**.
    
- Commands:
    
    `sudo pacman -Sc yay -Sc`
    

### 5. **Clear All Package Cache (Aggressive)**

- Removes **all cached packages**, even those currently installed.
    
- Use with caution.
    
- Commands:
    
    `sudo pacman -Scc yay -Scc`
    

---

## 🧼 Dependency and Orphan Management

### 6. **Remove Unused Dependencies**

- Command:
    
    `yay -Yc`
    

### 7. **List and Remove Orphaned Packages**

- Check for orphans:
    
    `pacman -Qdtq`
    
- Remove orphans:
    
    `sudo pacman -Rns $(pacman -Qdtq)`
    
- ⚠️ Note: Fish shell users should run this in Bash due to `$()` syntax.
    

---

## 🗃️ Directory Cleanup

### 8. **Clear Home Cache Directory**

- Check size:
    
    `du -sh ~/.cache`
    
- Remove contents:
    
    `rm -rf ~/.cache/*`
    

### 9. **Review Config Directory**

- Check size:
    
    `du -sh ~/.config`
    
- Remove unused config files with caution.
    
- These typically contain user settings; backup if unsure.