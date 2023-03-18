# vite-debug
minimal reproduction for bug

This is a react template create using `npm create vite@latest`.

Setting a breakpoint on any line and trying to start a debug session hangs and never completes.

Solution:
    1. Update the version of VSCode
    2. Add the following to the launch.json
       ```
       "sourceMaps": true,
        "resolveSourceMapLocations": [
            "${workspaceFolder}/**",
            "!**/node_modules/**"
        ]
       ```