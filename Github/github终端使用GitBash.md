## 问题:在VsCode的终端中使用GitBash，默认情况下是powershell
### 打开VsCode==设置==,位于左下角,再搜索框中输入==shell windows==，然后点击编辑==setting.json==
在大括号中添加入base.exe的路径,位于bin目录下,代码如下:
```javascript
     
     "terminal.integrated.profiles.windows": {
        "PowerShell": {  //Vscode默认的终端
            "source": "PowerShell",
            "icon": "terminal-powershell"
        },
        "Command Prompt": { //Cmd
            "path": [
                "${env:windir}\\Sysnative\\cmd.exe",
                "${env:windir}\\System32\\cmd.exe"
            ],
            "args": [],
            "icon": "terminal-cmd"
        },
        "GitBash":{
            "path":[
                "D:\\Git\\Git\\bin\\bash.exe"  //Bash.exe路径              
             ],
            "args": []      
            // "source": ""
          
        }
    },
    "terminal.integrated.defaultProfile.windows": "GitBash"
   ```

   ==注:== GitBash不能分开写Git Bash会不识别失效.