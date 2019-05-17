<!--
https://pypi.org/project/readme-generator/
https://pypi.org/project/python-readme-generator/
-->

[![](https://img.shields.io/badge/OS-Unix-blue.svg?longCache=True)]()
[![](https://img.shields.io/pypi/v/launchd-add-logs.svg?maxAge=3600)](https://pypi.org/project/launchd-add-logs/)
[![Travis](https://api.travis-ci.org/looking-for-a-job/launchd-add-logs.svg?branch=master)](https://travis-ci.org/looking-for-a-job/launchd-add-logs/)

#### Installation
```bash
$ [sudo] pip install launchd-add-logs
```

#### How it works
```
~/Library/Logs/LaunchAgents/<Label>/out.log
~/Library/Logs/LaunchAgents/<Label>/err.log
```

`<name>.plist`
```xml
<key>StandardErrorPath</key>
<string>/Users/<username>/Library/Logs/LaunchAgents/<Label>/err.log</string>
<key>StandardOutPath</key>
<string>/Users/<username>/Library/Logs/LaunchAgents/<Label>/out.log</string>
```

#### Scripts usage
command|`usage`
-|-
`launchd-add-logs` |`usage: launchd-add-logs path ...`

#### Examples
```bash
$ find ~/Library/LaunchAgents -name "*.plist" -print0 | xargs -0 launchd-add-logs
```

<p align="center">
    <a href="https://pypi.org/project/python-readme-generator/">python-readme-generator</a>
</p>