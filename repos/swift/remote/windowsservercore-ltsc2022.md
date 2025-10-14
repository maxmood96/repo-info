## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:aa83490a57b26bae017e5790e9a50a3914c5ce991a37072ec0b2439d8eab33cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull swift@sha256:b0a8aa0744a61e66d597d4c28d0e715abfb2a99ad7b502c34e0faf7d1d5d2f0a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5876482192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b176485745c74b97e191df4f90400b16a19f5ead5458b059b05ff11f8c6b5dee`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:52:26 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 14 Oct 2025 20:52:26 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Tue, 14 Oct 2025 20:52:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:52:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:52:28 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Tue, 14 Oct 2025 20:52:29 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Tue, 14 Oct 2025 20:53:16 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 14 Oct 2025 20:53:17 GMT
ARG PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe
# Tue, 14 Oct 2025 20:53:18 GMT
ARG PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
# Tue, 14 Oct 2025 20:53:53 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY39});                  Invoke-WebRequest -Uri ${env:PY39} -OutFile python-3.9.13-amd64.exe;            Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY39_SHA256});    $Hash = Get-FileHash python-3.9.13-amd64.exe -Algorithm sha256;                 if ($Hash.Hash -eq ${env:PY39_SHA256}) {                                          Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.9.13-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.9.13-amd64.exe;                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 14 Oct 2025 20:53:53 GMT
ARG VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe
# Tue, 14 Oct 2025 20:53:54 GMT
ARG VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
# Tue, 14 Oct 2025 21:03:32 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 14 Oct 2025 21:03:33 GMT
ARG SWIFT=https://download.swift.org/swift-6.2-release/windows10/swift-6.2-RELEASE/swift-6.2-RELEASE-windows10.exe
# Tue, 14 Oct 2025 21:03:33 GMT
ARG SWIFT_SHA256=80FBBC17D4F9EDEC74A83ABBEFEB9FF418FFC2158CD347111583C45E47F9789B
# Tue, 14 Oct 2025 21:07:15 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D SWIFT=https://download.swift.org/swift-6.2-release/windows10/swift-6.2-RELEASE/swift-6.2-RELEASE-windows10.exe SWIFT_SHA256=80FBBC17D4F9EDEC74A83ABBEFEB9FF418FFC2158CD347111583C45E47F9789B VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 14 Oct 2025 21:07:15 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512f6b55983610901b86450ae83bdef3ed270198876993d34fd529600470d8c`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93e875fec7fe88613220f7c25867c959779500e1f15322e2210aad378d656b6`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98eada989903941c90860396e5a4be62d3e47cbe8a250665c3dbb651bf6aba3d`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc1e119a96fbfb81a32940289b1cc6714cdcd8e1882f2b387f15d3bd24c52de`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f2f7edd1010e9a39e63cdf0fa3519541ccc49d3ea72c0f777772efa4a3008`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67424f84e74402e299fade93a4a963aa2a7aad0bad727240954a8f5ee05d5bc`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b409ca5b43edbfbdd1a50db782fd6dfd5cfa4afcc443708d98d9d1d6b90b8`  
		Last Modified: Tue, 14 Oct 2025 22:13:55 GMT  
		Size: 150.3 MB (150325128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b33bce83a368963dee9f5f21618d1a8e287fbbeb3f1f583e1ca3bc0f6b206`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9c311a892ed2cb73d4c40a24865d1a758dc0231cd70b8cfdb9e6ab072a6a0`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a75e6185b7a138b53fead4c9142c618e0d06ff7cd3188b26ef203afa1748f9`  
		Last Modified: Tue, 14 Oct 2025 21:11:24 GMT  
		Size: 47.9 MB (47896549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839d9329156d0100a5c5a716ba55979b1511dc5bbbaff51505cf1e8a7ec66ea7`  
		Last Modified: Tue, 14 Oct 2025 21:11:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d8062fe1000e6abe951c0c453eea60a34da8d0228be0ba2ec93745e1e8c8bb`  
		Last Modified: Tue, 14 Oct 2025 21:11:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ccfffd499285edca5463ee485fbbc4be90be2284b66dbfcc46791923a364f7`  
		Last Modified: Tue, 14 Oct 2025 22:49:12 GMT  
		Size: 1.7 GB (1686874279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabe23654310a5f4ba8f50e2d58dd00e65f0ac9890ccd3d2fc0b4e0fbfd39b13`  
		Last Modified: Tue, 14 Oct 2025 21:11:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dfdaf6a0da91e01716ee32475adb19963fda56ad967e90ed55e99c1a59219a`  
		Last Modified: Tue, 14 Oct 2025 21:11:12 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c71daaf2fd86b116973c257d4d1ff37f7f1395a3ed7ca90392fe5148968ac`  
		Last Modified: Tue, 14 Oct 2025 22:49:38 GMT  
		Size: 2.5 GB (2502349994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f35cc1c9a69a32ae9452666d95f39a7debe3e4959273bff1065db110db4ad6`  
		Last Modified: Tue, 14 Oct 2025 21:11:12 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
