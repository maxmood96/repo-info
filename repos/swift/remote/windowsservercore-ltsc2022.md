## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:7bae8a24df8fad972f558ec4881573df1b23ed9dfd3930f62424e2503b15f507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull swift@sha256:4d1c32f8d0cf6bce834245e93f6e4dd3cab859dc87cdbeddc9bc768e08c661af
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5965300644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db543cd74eca9611503a9f3ef07e3d85da1e17341c8a4165cf3531f9840677f`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:26:37 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 24 Oct 2025 18:26:38 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Fri, 24 Oct 2025 18:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:39 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 24 Oct 2025 18:26:39 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Fri, 24 Oct 2025 18:26:40 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Fri, 24 Oct 2025 18:27:44 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Fri, 24 Oct 2025 18:27:44 GMT
ARG PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe
# Fri, 24 Oct 2025 18:27:45 GMT
ARG PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
# Fri, 24 Oct 2025 18:28:23 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY39});                  Invoke-WebRequest -Uri ${env:PY39} -OutFile python-3.9.13-amd64.exe;            Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY39_SHA256});    $Hash = Get-FileHash python-3.9.13-amd64.exe -Algorithm sha256;                 if ($Hash.Hash -eq ${env:PY39_SHA256}) {                                          Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.9.13-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.9.13-amd64.exe;                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Fri, 24 Oct 2025 18:28:23 GMT
ARG VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe
# Fri, 24 Oct 2025 18:28:24 GMT
ARG VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
# Fri, 24 Oct 2025 18:38:55 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Fri, 24 Oct 2025 18:38:56 GMT
ARG SWIFT=https://download.swift.org/swift-6.2-release/windows10/swift-6.2-RELEASE/swift-6.2-RELEASE-windows10.exe
# Fri, 24 Oct 2025 18:38:57 GMT
ARG SWIFT_SHA256=80FBBC17D4F9EDEC74A83ABBEFEB9FF418FFC2158CD347111583C45E47F9789B
# Fri, 24 Oct 2025 18:42:41 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D SWIFT=https://download.swift.org/swift-6.2-release/windows10/swift-6.2-RELEASE/swift-6.2-RELEASE-windows10.exe SWIFT_SHA256=80FBBC17D4F9EDEC74A83ABBEFEB9FF418FFC2158CD347111583C45E47F9789B VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Fri, 24 Oct 2025 18:42:43 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d3b407a40004f4378d99f8daba2a40e46f2cf13a13af19ddf2047e45aba1aa`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea6099684cb76437299ae3637290bc406c7d867826aaca6e28b61e4adda9905`  
		Last Modified: Fri, 24 Oct 2025 18:46:37 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c21520f0f7e85537427d8cd8c39df3a49489d9dcfbd36e3cb20c7e9932dda1`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607c1723d53a815b2a91e381351cdc563735e8cf2f523bc0af3191c4d63fd8e7`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7007db907cf98f8797f37231b319ee8e467d9cc852ff2c94f2c462dc564af291`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bead70dcd30d5ccdaf82aa2a052590e2f093aef705f0c07e23984c8e6accf072`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137b9de45ca3f6222445ac0a406f563f2c8d0184332f4cba8eb34bf599bfe7e9`  
		Last Modified: Fri, 24 Oct 2025 19:48:45 GMT  
		Size: 150.5 MB (150467046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d1539bd82d63a4bae26155a3a988b51f8b135822637f61cf1ca2c70096df1f`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcce0d718dca94afca3f06c239645ffa1228f1669afc2ff91ff3bddae771c4a7`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa57b871fd21827f48f73450ff983d8600879b711b61af9481389893ddf341`  
		Last Modified: Fri, 24 Oct 2025 18:46:42 GMT  
		Size: 47.9 MB (47894577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0220479b2ee9ffff85e7fdbde928c0b782c5e789b01c5e49d776dbfa74acc4`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7073c3855cea6c5a25fc1e9e8c87d42c79ae8e11ce51fef02f3e1a841b3502cf`  
		Last Modified: Fri, 24 Oct 2025 18:46:37 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ca2deac360b40e29da3769117fbc927161b760f08a1dd44093acc6ba2b2f2`  
		Last Modified: Fri, 24 Oct 2025 19:50:39 GMT  
		Size: 1.7 GB (1687377251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c18eb65a0d25c0976111787350d2aa103f03f2077cc60ea3a92c5d3470155`  
		Last Modified: Fri, 24 Oct 2025 18:46:38 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677683114ff791344ad4212781f79e7ae540e1158b906f4948fb05bae7722496`  
		Last Modified: Fri, 24 Oct 2025 18:46:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01195224bb320aaea797e49abf9db9eb6cc9603bca91c50282b584607f55b726`  
		Last Modified: Fri, 24 Oct 2025 19:50:41 GMT  
		Size: 2.5 GB (2502351825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6e61899fbccf12d82489a8640cf4ece6e75d68da895a46b94bccc5d6e32397`  
		Last Modified: Fri, 24 Oct 2025 18:46:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
