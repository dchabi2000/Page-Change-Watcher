# Page Change Watcher  
A small English-language tool that checks web pages every 60 seconds and shows a Windows alert when any page content changes.

## Features

- Checks pages every 1 minute.
- Detects content change using SHA-256 hash.
- Shows a native Windows alert popup when a change is found.
- Stores previous hashes in `state.json`.

## Project Files

- `monitor_pages.py`: Main watcher app.
- `urls.txt`: URLs to monitor (one URL per line).
- `build_exe.bat`: Builds the EXE using PyInstaller.
- `requirements.txt`: Build dependencies.

## How To Use

1. Edit `urls.txt` and add your pages:

```txt
https://example.com
https://news.ycombinator.com
```

2. Run from source:

```powershell
py monitor_pages.py
```

3. Build EXE:

```powershell
build_exe.bat
```

4. Run the generated file:

```powershell
dist\PageChangeWatcher.exe
```

## Publish To GitHub With Tag

```powershell
git init
git add .
git commit -m "Initial release: Page Change Watcher"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
git push -u origin main
git tag -a v1.0.0 -m "First release"
git push origin v1.0.0
```

This creates a release tag `v1.0.0` that you can use for publishing.
