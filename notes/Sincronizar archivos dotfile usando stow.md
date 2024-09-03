# Sincronizar archivos dotfile usando stow

## Código

```bash
cd ~/.dotfiles
stow zsh
```

## Pasos

1. Ir al directorio de los dotfiles, (ej. `~/.dotfiles`)
2. Crear el nuevo archivo de configuración (ej. `~/.wezterm.lua`)
3. Correr el comando `stow wezterm.lua`, o simplemente `stow .` (Stow automatically ignores certain files, such as the .git directory.)
