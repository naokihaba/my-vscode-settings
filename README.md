# naokihaba vscode settings

Personal VS Code configuration files.

## 📁 File Structure

```
.vscode/
├── settings.json         # Editor settings
├── extensions.json       # Recommended extensions
└── global.code-snippets  # Code snippets
```

## 🚀 Usage

### settings.json

**As global settings:**

1. Open VS Code and press `Cmd + Shift + P` (Mac) / `Ctrl + Shift + P` (Windows/Linux)
2. Select `Preferences: Open User Settings (JSON)`
3. Copy and paste the contents of `.vscode/settings.json`

**As project settings:**

```bash
cp .vscode/settings.json <your-project>/.vscode/settings.json
```

### extensions.json

**Install recommended extensions:**

1. Clone this repository
2. Open the folder in VS Code
3. Go to Extensions tab and install from "Recommended" section

Or via command line:

```bash
$ cat .vscode/extensions.json | grep -o '"[^"]*\.[^"]*"' | tr -d '"' | xargs -I {} code --install-extension {}
```

### global.code-snippets

**As global snippets:**

1. Open VS Code and press `Cmd + Shift + P` (Mac) / `Ctrl + Shift + P` (Windows/Linux)
2. Select `Snippets: Configure User Snippets`
3. Select `New Global Snippets file...`
4. Copy and paste the contents of `.vscode/global.code-snippets`

**As project snippets:**

```bash
$ cp .vscode/global.code-snippets <your-project>/.vscode/
```

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| Settings not applied | Restart VS Code |
| Extension conflicts | Launch with `code --disable-extensions` |
| Snippets not showing | Check if `editor.quickSuggestions` is enabled |
