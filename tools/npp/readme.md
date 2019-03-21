# notepad++

## v7.6.3 - 64-bit 에 codealignment 플러그인 적용

[code alignment plugin got disabled in in the new version release](https://notepad-plus-plus.org/community/topic/17125/code-alignment-plugin-got-disabled-in-in-the-new-version-release)

RAMA-KRISHNA 부분 참고

**important: do not change anything else on your notepad++ installation, unless instructed by @PeterJones , me, or another community regular from here, or else any guides will not work, as we do not have tracks of your recent changes.**

**guide to install the code alignment npp plugin on your system with exactly this configuration:**

note: this guide will not work, if you changed your configuration again.

```
Notepad++ v7.6.3 (64-bit)
Build time : Jan 27 2019 - 17:16:47
Path : C:\Program Files\Notepad++\notepad++.exe
Admin mode : OFF
Local Conf mode : OFF
OS : Windows 10 (64-bit)
Plugins : ComparePlugin.dll DSpellCheck.dll mimeTools.dll NppConverter.dll NppTextFX.dll PluginManager.dll ViSimulator.dll
```
-----------------------------------------

- make sure you follow all steps precisely:
- download CodeAlignmentNpp_v14.1_x64.zip from [>>> here <<<](https://github.com/cpmcgrath/codealignment/releases/download/v14.1/CodeAlignmentNpp_v14.1_x64.zip).
- extract CodeAlignmentNpp_v14.1_x64.zip to your desktop and open it in an explorer window.
- open another explorer window and go to C:\Program Files\Notepad++\plugins
- create a new folder CodeAlignmentNpp inside of plugins

note: the folder name has to be written exactly like that.

(the resulting folder is C:\Program Files\Notepad++\plugins\CodeAlignmentNpp)

- copy CodeAlignmentNpp.dll from your downloaded “CodeAlignmentNpp_v14.1_x64” folder to C:\Program Files\Notepad++\plugins\CodeAlignmentNpp.

- copy the folder CodeAlignment from your downloaded “CodeAlignmentNpp_v14.1_x64” folder to C:\Program Files\Notepad++\plugins\CodeAlignmentNpp.

- restart notepad++ and your Code Alignment plugin is ready to go.

**important note: please remove your PluginManager.dll, as it is incompatible with notepad++ 7.6.3 and will write files to the wrong loctions.**

(remove the folder C:\Program Files\Notepad++\plugins\PluginManager completely)
