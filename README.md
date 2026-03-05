# 🪟 Komorebi Configuration

Configuration I use in Komorebi when using Windows 11

# komorebi.json

```json

{
  "$schema": "https://raw.githubusercontent.com/LGUG2Z/komorebi/v0.1.40/schema.json",
  "app_specific_configuration_path": "$Env:USERPROFILE/applications.json",
  "window_hiding_behaviour": "Cloak",
  "cross_monitor_move_behaviour": "Insert",
  "default_workspace_padding": 3,
  "default_container_padding": 3,
  "border": false,
  "border_width": 8,
  "border_offset": -1,
  "border_style": "System",
  "border_colours": {
    "single": "#42a5f5",
    "stack": "#00a542",
    "monocle": "#ff3399",
    "unfocused": "#808080"
  },
  "animation": {
    "enabled": true,
    "duration": 125,
    "fps": 60,
    "style": "EaseOutSine"
  },
  "floating_applications": [
    { "kind": "Exe", "id": "Blip.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "Everything.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "Photos.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "ApplicationFrameHost.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "explorer.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "lghub.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "NanaZip.Modern.FileManager.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "obs64.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "PowerToys.Settings.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "s3drive.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "whispering.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "ABDownloadManager.exe", "matching_strategy": "Equals" },
    { "kind": "Exe", "id": "TIDAL.exe", "matching_strategy": "Equals" }
  ],
  "manage_rules": [
    { "kind": "Exe", "id": "claude.exe", "matching_strategy": "Equals" }
  ],
  "monitors": [
    {
      "workspaces": [
        { "name": "I", "layout": "BSP" },
        { "name": "II", "layout": "BSP" },
        { "name": "III", "layout": "BSP" }
      ]
    }
  ]
}
```

# whkdrc

```plain text

.shell cmd

# ==========================================
# SISTEMA E WHKD
# ==========================================
# Recarregar o próprio WHKD (Motor de atalhos)
alt + o                 : taskkill /f /im whkd.exe && start /b whkd

# Recarregar configuração do Komorebi sem matar o app
alt + shift + o         : komorebic reload-configuration

# Cheat Sheet (Ajuda)
alt + i                 : komorebic toggle-shortcuts

# ==========================================
# NAVEGAÇÃO BÁSICA (Foco)
# ==========================================
alt + left              : komorebic focus left
alt + down              : komorebic focus down
alt + up                : komorebic focus up
alt + right             : komorebic focus right

# ==========================================
# MANIPULAÇÃO ESPACIAL (Mover e Alterar)
# ==========================================
alt + shift + left      : komorebic move left
alt + shift + down      : komorebic move down
alt + shift + up        : komorebic move up
alt + shift + right     : komorebic move right

# Fechar e Minimizar
alt + q                 : komorebic close
alt + w                 : komorebic minimize

# Alternar Estados
alt + t                 : komorebic toggle-float
alt + shift + f         : komorebic toggle-monocle

# Resize (Ajuste fino do tamanho das janelas)
alt + oem_plus          : komorebic resize-axis horizontal increase
alt + oem_minus         : komorebic resize-axis horizontal decrease
alt + shift + oem_plus  : komorebic resize-axis vertical increase
alt + shift + oem_minus : komorebic resize-axis vertical decrease

# ==========================================
# CONTROLE DE WORKSPACES (Os 3 Essenciais)
# ==========================================
alt + 1                 : komorebic focus-workspace 0
alt + 2                 : komorebic focus-workspace 1
alt + 3                 : komorebic focus-workspace 2

# Enviar janela focada para outro Workspace
alt + shift + 1         : komorebic move-to-workspace 0
alt + shift + 2         : komorebic move-to-workspace 1
alt + shift + 3         : komorebic move-to-workspace 2
```
