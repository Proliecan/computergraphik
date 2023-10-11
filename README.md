# I noe learn computer graphics

## Dependencies
- `freeglut3-dev`
- `mesa-common-dev`
- `mesa-utils`
- (`xorg-dev`)
- (`xorg`)

## Compiling with `g++`
```bash
g++ main.cpp -lglut -lGL -lGLU -fdiagnostics-color=always -o main
```

## Compiling (& launching) in VSCode
Example task.json:

```json
{
    "tasks": [
        {
            "type": "cppbuild",
            "label": "C/C++: g++ build active file",
            "command": "/usr/bin/g++",
            "args": [
                "${file}",
                "-lglut",
                "-lGL",
                "-lGLU",
                "-fdiagnostics-color=always",
                "-o",
                "${workspaceFolder}/out/${fileBasenameNoExtension}"
            ],
            "options": {
                "cwd": "${fileDirname}"
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "detail": "This just works. Trust me. But only for one file. The active one. THE ONE TO RULE THEM ALL."
        }
    ],
    "version": "2.0.0"
}
```