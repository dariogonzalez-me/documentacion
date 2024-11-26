# Instalando ZSH

## Zsh?

Oh My Zsh es un framework para Zsh (Z shell).

- Para que Oh My Zsh funcione, se debe instalar **Zsh**
    - ejecuta ` zsh --version `
    - Se espera `zsh 5.x.x` o mas reciente

- Ademas, Zsh deberia ser el shell predeterminado
    - Ejecuta ` echo $SHELL `
    - Se espera ` /usr/bin/zsh `

**Instalar zsh:**
```shell
sudo dnf install zsh
zsh --version
```

**Establecer zsh como predeterminado:**
```shell
sudo lchsh $USER
# /bin/zsh
```
> No funciona si Zsh no esta en `/etc/shells` o no tienes permisos para usar `chsh`

## Instalar Oh My zsh

Prerequisitos:
1. Zsh debe star instalado
2. instalar `curl` o `wget`
3. `git` debe estar instalado

**Instalacion basica:**
wget:
```shell
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
