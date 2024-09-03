# DSA-With-CPP
In Vscode for running any cpp file use cmd+shift+B and give input in input.txt and see output in output.txt

Tasks.json for windows 

{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Compile and run",
      "type": "shell",
      "command": "cmd",
      "args": [
        "/C",
        "g++ \"${file}\" -o \"${fileDirname}\\${fileBasenameNoExtension}\" && \"${fileDirname}\\${fileBasenameNoExtension}\" < \"${workspaceFolder}\\input.txt\" > \"${workspaceFolder}\\output.txt\""
      ],
      "presentation": {
        "reveal": "never"
      },
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "problemMatcher": {
        "owner": "cpp",
        "fileLocation": [
          "relative",
          "${workspaceRoot}"
        ],
        "pattern": {
          "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
          "file": 1,
          "line": 2,
          "column": 3,
          "severity": 4,
          "message": 5
        }
      }
    }
  ]
}

Tasks.json for macos 

