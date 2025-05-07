# ESP32 Template

This repository is a template based on [Hello World Example](https://github.com/espressif/esp-idf/tree/master/examples/get-started/hello_world) with

- [esp-idf](https://github.com/espressif/esp-idf) v5.4
- [ESP32 Arduino](https://github.com/espressif/arduino-esp32) 3.2.0

and a default `clang-format`/`clangd` configuration.

Change [Visual Studio Code Settings](.vscode/settings.json) accordingly, if needed.

I recommend to [install ESP-IDF from Git manually](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/linux-macos-setup.html).
([Windows user could also work with it with PowerShell](https://github.com/espressif/esp-idf/blob/master/install.ps1))

## Language Server

It's recommended to use [clangd](https://clangd.llvm.org/) as C/C++ language server.

If it's target is Xtensa platform, you MUST use espressif forked version of clangd.

see [Downloadable IDF Tools](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-guides/tools/idf-tools.html).

```bash
idf_tools.py install esp-clang
```

and change the clangd path (`clangd.path`) to `$ESP_CLANG_PATH/bin/clangd`.

## ESP32 Arduino

This repository is including [ESP32 Arduino](https://github.com/espressif/arduino-esp32) as a submodule.

If you want to use this template to create your own project, you need to clone
the repository recursively.  or run `git submodule update --init --recursive` to
initialize and update the submodules after cloning the repository.

If you don't need Arduino, delete the `components/arduino` directory and remove
the corresponding entry in `.gitmodules`.

## Note to me

```bash
> git submodule add https://github.com/espressif/arduino-esp32 components/arduino
Adding existing repo at 'components/arduino' to the index
```

## See More

- [Arduino as an ESP-IDF component](https://docs.espressif.com/projects/arduino-esp32/en/latest/esp-idf_component.html)
- [ESP-IDF Build System](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-guides/build-system.html)
