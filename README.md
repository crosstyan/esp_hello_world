# ESP32 Template

Expected to use with [esp-idf](https://github.com/espressif/esp-idf) v5.4 with [arduino-esp32](https://github.com/espressif/arduino-esp32) 3.2.0

Change [Visual Studio Code Settings](.vscode/settings.json) accordingly.

## Language Server

It's recommended to use [clangd](https://clangd.llvm.org/) as C/C++ language server.

If it's target is Xtensa platform, you MUST use espressif forked version of clangd.

see [Downloadable IDF Tools](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-guides/tools/idf-tools.html).

```bash
idf_tools.py install esp-clang
```

and change the clangd path (`clangd.path`) to `$ESP_CLANG_PATH/bin/clangd`.
