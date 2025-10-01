# dotfiles

Conjunto de configuraciones personales para macOS: **zsh**, **vim**, **git**, utilerías instaladas vía Homebrew, etc.
Gestionado con [Dotbot](https://github.com/anishathalye/dotbot) como submódulo para automatizar la creación de symlinks y la instalación.

---

## 🛠 Requisitos

- macOS (Catalina o superior recomendado)
- [Homebrew](https://brew.sh/) instalado
- (Opcional) Git configurado globalmente

---

## ⚙️ Instalación

> **Recomendación:** Haz un fork de este repositorio si quieres usarlo con tu propia configuración (por ejemplo, para modificar tu `gitconfig` antes de ejecutar `install`). Esto evita sobreescribir tu configuración actual.

Clona el repositorio en tu `$HOME` (o en `~/.dotfiles`).
Puedes hacerlo de dos formas:

### Opción 1: Clonado con submódulos (más sencillo)

```bash
git clone --recursive https://github.com/{tu-usuario}/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
./install
```

### Opción 2: Clonado normal + inicialización de submódulos

```bash
git clone https://github.com/{tu-usuario}/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
git submodule update --init --recursive
./install
```

El script `install` usará **Dotbot** para crear symlinks definidos en `install.conf.yaml` y ejecutar tareas adicionales (como instalar paquetes desde el `Brewfile`).

Para actualizar tu configuración:

```bash
cd ~/.dotfiles
git pull origin main
git submodule update --init --recursive
./install
```

---

## 📂 Estructura del proyecto

```
.
├── .editorconfig
├── .gitignore
├── .gitmodules
├── Brewfile
├── antigenrc
├── bash_profile
├── dotbot/
├── gitconfig
├── install
├── install.conf.yaml
├── p10k.zsh
├── profile
├── vimrc
├── zprofile
├── zshaliases
├── zshenv
└── zshrc
```

| Archivo / carpeta                                        | Propósito                                                                        |
| -------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `.editorconfig`                                          | Reglas de formato común                                                          |
| `.gitignore`                                             | Ignorados en el repositorio                                                      |
| `.gitmodules`                                            | Configuración de submódulos (incluye Dotbot)                                     |
| `Brewfile`                                               | Lista de paquetes/apps para Homebrew                                             |
| `antigenrc`                                              | Configuración de plugins Zsh con Antigen                                         |
| `bash_profile`, `profile`, `zprofile`, `zshrc`, `zshenv` | Configuraciones de shell                                                         |
| `zshaliases`                                             | Alias personalizados                                                             |
| `gitconfig`                                              | Configuración global de Git                                                      |
| `p10k.zsh`                                               | Configuración del tema [Powerlevel10k](https://github.com/romkatv/powerlevel10k) |
| `vimrc`                                                  | Configuración de Vim                                                             |
| `dotbot/`                                                | Submódulo con el motor de instalación                                            |
| `install`                                                | Script ejecutable que lanza Dotbot                                               |
| `install.conf.yaml`                                      | Archivo de configuración usado por Dotbot                                        |

---

## 🚀 Demo (opcional)

Puedes añadir capturas o GIFs mostrando tu terminal con el prompt de Powerlevel10k, por ejemplo:

```md
![Terminal demo](assets/terminal-demo.png)
```

---

## 💡 Personalización

- Edita el `Brewfile` para instalar únicamente los paquetes que uses.
- Modifica `install.conf.yaml` para agregar o quitar symlinks.
- Si algún archivo de configuración no lo quieres, elimínalo o coméntalo en el `install.conf.yaml`.

---

## 🧾 Licencia

MIT License
© [Tu Nombre] — 2025
