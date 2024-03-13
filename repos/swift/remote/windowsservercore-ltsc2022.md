## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:304eb8ed84449d66a5bfc88aebd8dd308a594392c332fb45423ff884b73b7852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull swift@sha256:5c49bf8eba57adfca169b9c085417feb795ac8e820d528a876404ce5d5362c2c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5392937761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1280a4aca22076d0f9106cb5f1f29e7b7882ad79b2d9e26af98fd6f66a601e`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 04:28:09 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 Mar 2024 04:28:10 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Wed, 13 Mar 2024 04:28:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:28:11 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 13 Mar 2024 04:28:12 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Wed, 13 Mar 2024 04:28:13 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Wed, 13 Mar 2024 04:30:00 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 Mar 2024 04:30:01 GMT
ARG PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe
# Wed, 13 Mar 2024 04:30:02 GMT
ARG PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
# Wed, 13 Mar 2024 04:31:23 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY39});                  Invoke-WebRequest -Uri ${env:PY39} -OutFile python-3.9.13-amd64.exe;            Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY39_SHA256});    $Hash = Get-FileHash python-3.9.13-amd64.exe -Algorithm sha256;                 if ($Hash.Hash -eq ${env:PY39_SHA256}) {                                          Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.9.13-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.9.13-amd64.exe;                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 Mar 2024 04:31:24 GMT
ARG VSB=https://aka.ms/vs/17/release/vs_buildtools.exe
# Wed, 13 Mar 2024 04:31:25 GMT
ARG VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
# Wed, 13 Mar 2024 04:47:52 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D VSB=https://aka.ms/vs/17/release/vs_buildtools.exe VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                         }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 Mar 2024 04:47:53 GMT
ARG SWIFT=https://download.swift.org/swift-5.10-release/windows10/swift-5.10-RELEASE/swift-5.10-RELEASE-windows10.exe
# Wed, 13 Mar 2024 04:47:54 GMT
ARG SWIFT_SHA256=A0E2B32DFB56FCB83D4FEC1D1FF4B43B4B0986EDE4C065FF52F336EA9AA49322
# Wed, 13 Mar 2024 04:51:44 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D SWIFT=https://download.swift.org/swift-5.10-release/windows10/swift-5.10-RELEASE/swift-5.10-RELEASE-windows10.exe SWIFT_SHA256=A0E2B32DFB56FCB83D4FEC1D1FF4B43B4B0986EDE4C065FF52F336EA9AA49322 VSB=https://aka.ms/vs/17/release/vs_buildtools.exe VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 13 Mar 2024 04:51:47 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa41c97ec479bf5b15ad8725e0b964152396a5c14c41bf3c75679b04d760fd2`  
		Last Modified: Wed, 13 Mar 2024 04:56:16 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb590f3e369dbb0db9321136cc47da35281bb83a89d5bdacba41604ecbeada5`  
		Last Modified: Wed, 13 Mar 2024 04:56:13 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef22244b056578650a07803c8b427518760b7255b4733e0f7c1e52726ad47e7e`  
		Last Modified: Wed, 13 Mar 2024 04:56:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b41a4afd67df82b198a47c97249386d46b73d82df82fa0e4a46fff6fa38a1c`  
		Last Modified: Wed, 13 Mar 2024 04:56:08 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e2bf527369bdd26325aa2a239582f6fd3e22f6869deac6dcd9be91b9ac8501`  
		Last Modified: Wed, 13 Mar 2024 04:56:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636c1a1af55ae161a2f0a49697ccb4355a90ae7ab020507f7454dc6aa87f9f4c`  
		Last Modified: Wed, 13 Mar 2024 04:56:04 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209b119d7025c30072005b058c7697f506d88f0ac3f1f9b5d0d0ac23f81767f2`  
		Last Modified: Wed, 13 Mar 2024 04:56:47 GMT  
		Size: 150.4 MB (150376662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a74407d62bc326122db1d572822b510e5459465427f2b50cbfa43adb5327f`  
		Last Modified: Wed, 13 Mar 2024 04:56:02 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1748f7a29904d73af0cde0a1b90ca920b315a3fd855d511e06d6b36f1c16ab4`  
		Last Modified: Wed, 13 Mar 2024 04:56:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e977ba35b81b36b9b263d2693c6ceac95c2a050a5992a4a1c1029f646e7f34`  
		Last Modified: Wed, 13 Mar 2024 04:56:14 GMT  
		Size: 47.8 MB (47804410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f65c8be17b0616f58e0e495e893773cead519576a0e92343106adc92d2a894`  
		Last Modified: Wed, 13 Mar 2024 04:56:00 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab55e7871fa65bc7a5a4abe6f272ca798decfc9fceece0ba9b7735a11bb740e`  
		Last Modified: Wed, 13 Mar 2024 04:56:00 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2caf7b6df0041d09c7643c7cc14d8c0a6e8b23f14c1ba9ac66a61ac7b561f5`  
		Last Modified: Wed, 13 Mar 2024 05:00:41 GMT  
		Size: 1.7 GB (1650702646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e120510bbe22e62521c5e3be5afbf6c21c656cf088634245d3bfcede47754`  
		Last Modified: Wed, 13 Mar 2024 04:55:58 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59ae7a929520ad601c2aebf0c6d2708adad6974a5e6f55365aa1f3949fec1e8`  
		Last Modified: Wed, 13 Mar 2024 04:55:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a538b7f78e27bc338b70ada90628b6dc19245b95d800147fb1f5339b11f5983`  
		Last Modified: Wed, 13 Mar 2024 05:00:16 GMT  
		Size: 1.6 GB (1586577051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f77dc71a0478f256d5cba480275a1e8c06c8ee7d858d6f3651b8e2e0c59792d`  
		Last Modified: Wed, 13 Mar 2024 04:55:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
