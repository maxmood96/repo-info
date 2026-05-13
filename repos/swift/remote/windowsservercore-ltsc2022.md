## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:f0916eaec1fd0f5f6c01a0fa25a221be772b3c9f60af4e4a2f46ee48d90218ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull swift@sha256:8fa651bec42d06f2ab7d16a75407e79d99e84ae63698455ddc1b2920ca4cfa5d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 GB (7099390094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec60bd35ea0a7e0ec0bd822703209e655dad799b5e13f765cbabebf0fb9bb52`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:58:57 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 12 May 2026 23:58:57 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Tue, 12 May 2026 23:58:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:59 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Tue, 12 May 2026 23:59:00 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Tue, 12 May 2026 23:59:45 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 12 May 2026 23:59:45 GMT
ARG PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe
# Tue, 12 May 2026 23:59:46 GMT
ARG PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B
# Wed, 13 May 2026 00:00:19 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY310});                 Invoke-WebRequest -Uri ${env:PY310} -OutFile python-3.10.11-amd64.exe;          Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY310_SHA256});    $Hash = Get-FileHash python-3.10.11-amd64.exe -Algorithm sha256;                if ($Hash.Hash -eq ${env:PY310_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.10.11-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.10.11-amd64.exe;                                    Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 May 2026 00:00:20 GMT
ARG VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe
# Wed, 13 May 2026 00:00:20 GMT
ARG VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
# Wed, 13 May 2026 00:09:48 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 May 2026 00:31:02 GMT
ARG SWIFT=https://download.swift.org/swift-6.3.1-release/windows10/swift-6.3.1-RELEASE/swift-6.3.1-RELEASE-windows10.exe
# Wed, 13 May 2026 00:31:02 GMT
ARG SWIFT_SHA256=E5A0E6B5BD8F8F3045B1D2420C06ECEB6B7918D800BEC3733CE4D657E7170F51
# Wed, 13 May 2026 00:35:35 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B SWIFT=https://download.swift.org/swift-6.3.1-release/windows10/swift-6.3.1-RELEASE/swift-6.3.1-RELEASE-windows10.exe SWIFT_SHA256=E5A0E6B5BD8F8F3045B1D2420C06ECEB6B7918D800BEC3733CE4D657E7170F51 VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 May 2026 00:35:36 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49de533cb0b1a6b44555e7e74f5811de5c6b24fe61d84af60a34aea3bd53c941`  
		Last Modified: Wed, 13 May 2026 00:13:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ae7a4b69a3f85deb8c80313bf9e92e8dfae936714dd59c3c76fd0ddc6856f2`  
		Last Modified: Wed, 13 May 2026 00:13:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746f3cfc6d35b2fe1156a9c7c74cb1b6b8b481353d7e0c7f28226a01cd3817ed`  
		Last Modified: Wed, 13 May 2026 00:13:51 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd58c385ef7deabf487a97c4961e4037d4a31ee91d25246024c4d0df8643ac78`  
		Last Modified: Wed, 13 May 2026 00:13:49 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24d3b9f333f6af0750fff6623440c44346f56cfee4d0bb7baf129176c473ccf`  
		Last Modified: Wed, 13 May 2026 00:13:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284765abf73094f698ef1c3d059b1eeefb3ab6a42401449dfb19aed9cb025fc2`  
		Last Modified: Wed, 13 May 2026 00:13:45 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6eff052465eb5e0e38d66fe7d29cefefb6007c70dc5ba3d670f978093b1f19`  
		Last Modified: Wed, 13 May 2026 00:14:06 GMT  
		Size: 150.4 MB (150440875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656a56ad114bebbdffdac16d8dc45e9bd68b9eedfca6c478bb8ec164d85fb6a7`  
		Last Modified: Wed, 13 May 2026 00:13:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ade5508807278befd3c69638f9eb5fdda9ac505d95e4510daf9c9edf04abab`  
		Last Modified: Wed, 13 May 2026 00:13:43 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bbf9e52ee03e0c15a7947a7aaa43f93167d20674926ebf3aa81b85545781f5`  
		Last Modified: Wed, 13 May 2026 00:13:49 GMT  
		Size: 46.2 MB (46243289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce740a89fe40521565372ad7801c9317847abecc81e1e1ecbd4012b75f0eba0c`  
		Last Modified: Wed, 13 May 2026 00:13:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835aa1f879d32354eba90137fca45fab353f9fdb76f31874c0cfdc46e0d3687`  
		Last Modified: Wed, 13 May 2026 00:13:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899dd646cf062d69967217418315f2535978a19707fc4f57ed65795cf469bc8f`  
		Last Modified: Wed, 13 May 2026 00:16:19 GMT  
		Size: 1.7 GB (1704097008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e2dd5cf38f6e25ec8fddc436dc3d3410dada8e2facc8addc65e2d2f9ae3005`  
		Last Modified: Wed, 13 May 2026 00:35:46 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e84b33a9d121b9c421e9d4664da7ac63d2a39c403c4cfe427495c33f2f13e0`  
		Last Modified: Wed, 13 May 2026 00:35:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70125f075c2aa16d3c4f53cd518dc7389129e331482c7383111c2e5358de4a7`  
		Last Modified: Wed, 13 May 2026 00:39:46 GMT  
		Size: 3.1 GB (3076171306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5d9318b5f053a9eb9378869495da59e8852a98d67232d4e5f051e985f0f6e6`  
		Last Modified: Wed, 13 May 2026 00:35:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
