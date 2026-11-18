# How to play / Как запустить

**[Русский](#русский) · [English](#english)**

---

## Русский

### Игры и файлы запуска

- **Meridian Coast (Godot)** (Godot 4.7.2): [MeridianCoast-Godot-Windows-x64.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Godot-Windows-x64.zip) → запустите `Meridian Coast.exe` · [MeridianCoast-Godot-macOS.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Godot-macOS.zip)
- **Meridian Coast (Unity)** (Unity 6000.6.0f1): [MeridianCoast-Unity-Windows-x64.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Unity-Windows-x64.zip) → запустите `MeridianCoast.exe` · [MeridianCoast-Unity-macOS.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Unity-macOS.zip)
- **Port Meridian (Unreal Engine 5)** (Unreal Engine 5.8): [PortMeridian-Unreal-Windows-x64.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/PortMeridian-Unreal-Windows-x64.zip) → запустите `Unreal_GTA.exe`

### Готовая сборка для Windows (1 файл)

1. Скачайте zip игры (ссылка выше или вкладка **Releases** справа на странице репозитория).
2. Нажмите по zip правой кнопкой → **Извлечь всё…** Не запускайте игру прямо из архива.
3. Откройте распакованную папку и дважды кликните `.exe` с названием игры. Всё — установка не нужна.
4. Если Windows показала «Windows защитила ваш компьютер» — это потому, что сборка не подписана платным сертификатом. Нажмите **Подробнее → Выполнить в любом случае**. Исходный код каждой игры лежит в этом репозитории.
5. Проверить, что файл не изменён: в PowerShell выполните `Get-FileHash .\ИмяФайла.zip` и сравните с `SHA256SUMS.txt` в релизе.

Требования: Windows 10/11 64-bit, видеокарта с поддержкой DirectX 12 / Vulkan. Для игр на Unreal Engine при ошибке про отсутствующие DLL установите Microsoft Visual C++ Redistributable (x64) с сайта Microsoft.

### macOS

Распакуйте zip/tar.gz, затем на приложении: правый клик → **Открыть** → **Открыть** (сборка не подписана Apple). Если macOS пишет, что приложение повреждено: `xattr -dr com.apple.quarantine /путь/к/Игра.app`, а если не помогло — `codesign --force --deep --sign - /путь/к/Игра.app`.

### Как открыть исходники в движке

**Godot (4.7.2):** скачайте Godot той же версии с godotengine.org (обычная версия, не .NET, если в проекте нет C#). В Project Manager нажмите **Import**, выберите `project.godot` в папке игры, затем **Run (F5)**. Первое открытие может занять пару минут — Godot импортирует ресурсы.

**Unity (6000.6.0f1):** установите Unity Hub и редактор этой версии. **Hub → Add → Add project from disk** → выберите папку игры (где лежат `Assets`, `Packages`, `ProjectSettings`). Первое открытие долгое — Unity создаёт папку `Library`. Откройте основную сцену (см. README игры или `File → Build Profiles`) и нажмите **Play**.

**Unreal Engine (5.8):** установите движок через Epic Games Launcher. Если в проекте есть папка `Source` (C++), нужна Visual Studio 2022 с компонентом «Разработка игр на C++». Дважды кликните `.uproject` и согласитесь пересобрать модули (или ПКМ по `.uproject` → *Generate Visual Studio project files*). Затем **Play** в редакторе.

### Сделать такую же игру с ИИ

Промпты лежат в папке [prompts/](prompts) (если есть), а гайд по связке Claude/Codex + движок + Blender MCP — в [BLENDER_MCP_GUIDE.md](BLENDER_MCP_GUIDE.md).

---

## English

### Games and launch files

- **Meridian Coast (Godot)** (Godot 4.7.2): [MeridianCoast-Godot-Windows-x64.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Godot-Windows-x64.zip) → run `Meridian Coast.exe` · [MeridianCoast-Godot-macOS.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Godot-macOS.zip)
- **Meridian Coast (Unity)** (Unity 6000.6.0f1): [MeridianCoast-Unity-Windows-x64.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Unity-Windows-x64.zip) → run `MeridianCoast.exe` · [MeridianCoast-Unity-macOS.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/MeridianCoast-Unity-macOS.zip)
- **Port Meridian (Unreal Engine 5)** (Unreal Engine 5.8): [PortMeridian-Unreal-Windows-x64.zip](https://github.com/Cryptopiy/GPT-6-Astra-Meridian-Coast-Unity-Godot-Unreal/releases/download/v1.0/PortMeridian-Unreal-Windows-x64.zip) → run `Unreal_GTA.exe`

### Ready-made Windows build (1 file)

1. Download the game's zip (link above or the **Releases** tab on the right side of the repo page).
2. Right-click the zip → **Extract All…** Do not run the game from inside the archive.
3. Open the extracted folder and double-click the `.exe` named after the game. That's it — no installation.
4. If Windows shows “Windows protected your PC”, it's because the build isn't signed with a paid certificate. Click **More info → Run anyway**. The full source code of every game is in this repo.
5. To verify the download: in PowerShell run `Get-FileHash .\FileName.zip` and compare with `SHA256SUMS.txt` in the release.

Requirements: Windows 10/11 64-bit, a GPU with DirectX 12 / Vulkan support. For Unreal Engine games, if you get a missing-DLL error, install the Microsoft Visual C++ Redistributable (x64) from Microsoft's website.

### macOS

Unzip, then right-click the app → **Open** → **Open** (the build is not notarized by Apple). If macOS says the app is damaged: `xattr -dr com.apple.quarantine /path/to/Game.app`; if that doesn't help — `codesign --force --deep --sign - /path/to/Game.app`.

### Open the source in the engine

**Godot (4.7.2):** download the same Godot version from godotengine.org (standard build, not .NET unless the project uses C#). In the Project Manager click **Import**, select `project.godot` in the game folder, then **Run (F5)**. The first import can take a couple of minutes.

**Unity (6000.6.0f1):** install Unity Hub and that editor version. **Hub → Add → Add project from disk** → pick the game folder (the one with `Assets`, `Packages`, `ProjectSettings`). The first open is slow — Unity rebuilds `Library`. Open the main scene (see the game's README or `File → Build Profiles`) and press **Play**.

**Unreal Engine (5.8):** install the engine via the Epic Games Launcher. If the project has a `Source` folder (C++), you need Visual Studio 2022 with the “Game development with C++” workload. Double-click the `.uproject` and agree to rebuild modules (or right-click it → *Generate Visual Studio project files*). Then press **Play** in the editor.

### Make a game like this with AI

The prompts are in [prompts/](prompts) (if present), and the Claude/Codex + engine + Blender MCP setup guide is in [BLENDER_MCP_GUIDE.md](BLENDER_MCP_GUIDE.md).
