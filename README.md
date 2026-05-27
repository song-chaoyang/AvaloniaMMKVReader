# MMKV Reader

[![.NET](https://img.shields.io/badge/.NET-9.0-512BD4)](https://dotnet.microsoft.com/)
[![Avalonia](https://img.shields.io/badge/Avalonia-11.3.9-8B44AC)](https://avaloniaui.net/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A cross-platform MMKV data file parser built with [Avalonia UI](https://avaloniaui.net/), inspired by [pengwei1024/MMKVReader](https://github.com/pengwei1024/MMKVReader).

> 中文说明请查看：[README.zh-CN.md](README.zh-CN.md)

## Features

- 🖥️ **Cross-platform support** - Windows, macOS, and Linux
- 📁 **Drag and drop** - Open MMKV data files and CRC files directly
- 🔍 **Multiple value types** - Auto/String/Int32/Int64/Float/Double/Bool/Bytes
- 🌙 **Dark theme** - Modern desktop UI with fluent styling
- 📊 **Structured table view** - Inspect parsed key-value data clearly

## Screenshots

|  |  |  |
|:---:|:---:|:---:|
| ![](screenshots/main.png) | ![](screenshots/main2.png) | ![](screenshots/main3.png) |

## Usage

### Option 1: Drag and drop files

Drag an MMKV data file, with an optional `.crc` file, directly into the application window.

### Option 2: Select a file manually

Click **Select Data File** and choose the MMKV file you want to inspect.

### Supported data types

Use the selector in the top-right corner to choose how values should be parsed:

- **Auto** - Detect type automatically (default)
- **String** - String values
- **Int32 / Int64** - Integer values
- **Float / Double** - Floating-point values
- **Bool** - Boolean values
- **Bytes** - Hexadecimal byte output

## Build and run

### Requirements

- [.NET 9.0 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)

### Run locally

```bash
# Clone the repository
git clone https://github.com/song-chaoyang/AvaloniaMMKVReader.git
cd AvaloniaMMKVReader

# Run the desktop app
dotnet run --project AvaloniaMMKVReader.Desktop
```

### Publish

```bash
# Windows
dotnet publish AvaloniaMMKVReader.Desktop -c Release -r win-x64 --self-contained

# macOS Intel
dotnet publish AvaloniaMMKVReader.Desktop -c Release -r osx-x64 --self-contained

# macOS Apple Silicon
dotnet publish AvaloniaMMKVReader.Desktop -c Release -r osx-arm64 --self-contained

# Linux
dotnet publish AvaloniaMMKVReader.Desktop -c Release -r linux-x64 --self-contained
```

## Project structure

```text
AvaloniaMMKVReader/
├── AvaloniaMMKVReader/           # Core library
│   ├── Models/                   # Data models
│   ├── Services/                 # MMKV parsing services
│   ├── ViewModels/               # MVVM view models
│   └── Views/                    # UI views
├── AvaloniaMMKVReader.Desktop/   # Desktop entry project
├── AvaloniaMMKVReader.Android/   # Android project (requires workload)
├── AvaloniaMMKVReader.iOS/       # iOS project (requires workload)
└── AvaloniaMMKVReader.Browser/   # Web project
```

## About MMKV

[MMKV](https://github.com/Tencent/MMKV) is Tencent's high-performance key-value storage framework and is widely used in mobile applications. This tool helps developers inspect MMKV-generated data files during debugging and analysis.

## License

MIT License

## Acknowledgements

- [Avalonia UI](https://avaloniaui.net/) - Cross-platform UI framework
- [pengwei1024/MMKVReader](https://github.com/pengwei1024/MMKVReader) - Original macOS version
- [Tencent/MMKV](https://github.com/Tencent/MMKV) - MMKV storage framework
