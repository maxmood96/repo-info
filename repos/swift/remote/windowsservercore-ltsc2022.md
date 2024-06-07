## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:868be80a790baefca61be4f9ef01cc33c8766598e6f05c86fcf1f043afe36197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull swift@sha256:66c8e96b815703ef73218673e7e84e8670330e7e50f57e316d42d4dd7d48bf6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5548163069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dea13160004a22688d34220081448308f392ffebbf9edaaa03fd6f4a75a74e9`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 23:08:05 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 May 2024 23:08:06 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Wed, 15 May 2024 23:08:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 23:08:08 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 15 May 2024 23:08:08 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Wed, 15 May 2024 23:08:09 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Wed, 15 May 2024 23:10:00 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 15 May 2024 23:10:01 GMT
ARG PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe
# Wed, 15 May 2024 23:10:02 GMT
ARG PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
# Wed, 15 May 2024 23:11:26 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY39});                  Invoke-WebRequest -Uri ${env:PY39} -OutFile python-3.9.13-amd64.exe;            Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY39_SHA256});    $Hash = Get-FileHash python-3.9.13-amd64.exe -Algorithm sha256;                 if ($Hash.Hash -eq ${env:PY39_SHA256}) {                                          Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.9.13-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.9.13-amd64.exe;                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 15 May 2024 23:11:27 GMT
ARG VSB=https://aka.ms/vs/17/release/vs_buildtools.exe
# Wed, 15 May 2024 23:11:28 GMT
ARG VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
# Wed, 15 May 2024 23:28:21 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D VSB=https://aka.ms/vs/17/release/vs_buildtools.exe VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                         }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Fri, 07 Jun 2024 01:15:56 GMT
ARG SWIFT=https://download.swift.org/swift-5.10.1-release/windows10/swift-5.10.1-RELEASE/swift-5.10.1-RELEASE-windows10.exe
# Fri, 07 Jun 2024 01:15:56 GMT
ARG SWIFT_SHA256=3027762138ACFA1BBE3050FF6613BBE754332E84C9EFA5C23984646009297286
# Fri, 07 Jun 2024 01:19:09 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D SWIFT=https://download.swift.org/swift-5.10.1-release/windows10/swift-5.10.1-RELEASE/swift-5.10.1-RELEASE-windows10.exe SWIFT_SHA256=3027762138ACFA1BBE3050FF6613BBE754332E84C9EFA5C23984646009297286 VSB=https://aka.ms/vs/17/release/vs_buildtools.exe VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Fri, 07 Jun 2024 01:19:12 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e62bba1c81f5d22e29a7394f73b2c2c299fe3e2ac52d0d3ffc584eead4cc783`  
		Last Modified: Wed, 15 May 2024 23:36:43 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab3e612e9c2165f071a4c99c51124edc226ace697eb166964d3455f75ad33dc`  
		Last Modified: Wed, 15 May 2024 23:36:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760241db23854079abf5f525816ab2c11f160af2a94dff4594e2ade665fd325`  
		Last Modified: Wed, 15 May 2024 23:36:39 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64126c1559401ef32532e7f19fab84efbf1f50889f15de36f3d942a05b1bffdb`  
		Last Modified: Wed, 15 May 2024 23:36:37 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fb7befcf43e1035c91fba99a4932b6d834bf25fde70cad42d3926d7fb8c78b`  
		Last Modified: Wed, 15 May 2024 23:36:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da10a368dd9e20201fe554035537261ae4cbb16affb6c9214ea6147014b273`  
		Last Modified: Wed, 15 May 2024 23:36:32 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ddc0d10674099c40faff9403e963e780bc786a1d718543441f4dd1971de8d2`  
		Last Modified: Wed, 15 May 2024 23:37:14 GMT  
		Size: 150.2 MB (150243777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9884561c92a3373e3aba7dcd8380c22d0a966e74538b1b29b18e64229607a2eb`  
		Last Modified: Wed, 15 May 2024 23:36:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d32e8fe25fc9e3969ab19b78ef68557e54e784b2b870a22b81b2f90a6d2a94`  
		Last Modified: Wed, 15 May 2024 23:36:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2b927a84d3b112ac803b2daa4cbc449a8d921345b895129fa8a34f1b5f591b`  
		Last Modified: Wed, 15 May 2024 23:36:40 GMT  
		Size: 47.8 MB (47798917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7903beb2905eb5887c858395c3677b1412bd66839c3f696ecfc22966917862ad`  
		Last Modified: Wed, 15 May 2024 23:36:27 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3912a8187e879cf95bee9f8d37ae05061aa5a5612c4f51751cb7658185c36b4e`  
		Last Modified: Wed, 15 May 2024 23:36:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f78ec29c359017e6e4f55200b4398ef905647995086ac6acbd1cc3b5eb3f276`  
		Last Modified: Wed, 15 May 2024 23:41:03 GMT  
		Size: 1.7 GB (1650961982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09eeb961b59e54b875edba642e9b244f446d9162fc980a7aa54d3c3603b45d6`  
		Last Modified: Fri, 07 Jun 2024 01:19:43 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b198efe489468515c75ba02c8c83ec416fd69315f4dfdea854cea7134b15648`  
		Last Modified: Fri, 07 Jun 2024 01:19:43 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e98665db6ca6fcd7debde83284bf4374dfe132831592ec50e5ca327c5fe815`  
		Last Modified: Fri, 07 Jun 2024 01:23:18 GMT  
		Size: 1.6 GB (1586468651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c3e7477729e6be1319b9b6d740b10916e6f627f954ebc5fd0481f27d07e1d`  
		Last Modified: Fri, 07 Jun 2024 01:19:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
