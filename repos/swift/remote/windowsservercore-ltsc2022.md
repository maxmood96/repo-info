## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:2abdaafb0f0ce6342d91e78f997ebbae921ddae2dad716502b9ed44dcacffd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull swift@sha256:e3a90c09e84228f60f446bdcaa1b07510a1b55dc6728ec2a74dcd2c1f21e6113
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6103148898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b487757401878eaba4d31a4f6f84e2509dc3b1c3f4a553528de247c36ff0de`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 23:10:02 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 14 Feb 2024 23:10:03 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Wed, 14 Feb 2024 23:10:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 23:10:04 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Feb 2024 23:10:05 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Wed, 14 Feb 2024 23:10:06 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Wed, 14 Feb 2024 23:11:59 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 14 Feb 2024 23:12:00 GMT
ARG PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe
# Wed, 14 Feb 2024 23:12:01 GMT
ARG PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
# Wed, 14 Feb 2024 23:13:20 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY39});                  Invoke-WebRequest -Uri ${env:PY39} -OutFile python-3.9.13-amd64.exe;            Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY39_SHA256});    $Hash = Get-FileHash python-3.9.13-amd64.exe -Algorithm sha256;                 if ($Hash.Hash -eq ${env:PY39_SHA256}) {                                          Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.9.13-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.9.13-amd64.exe;                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 14 Feb 2024 23:13:21 GMT
ARG VSB=https://aka.ms/vs/17/release/vs_buildtools.exe
# Wed, 14 Feb 2024 23:13:22 GMT
ARG VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
# Wed, 14 Feb 2024 23:29:38 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D VSB=https://aka.ms/vs/17/release/vs_buildtools.exe VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                         }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 14 Feb 2024 23:29:40 GMT
ARG SWIFT=https://download.swift.org/swift-5.9.2-release/windows10/swift-5.9.2-RELEASE/swift-5.9.2-RELEASE-windows10.exe
# Wed, 14 Feb 2024 23:29:41 GMT
ARG SWIFT_SHA256=D78A717551C78E824C9B74B0CFB1AD86060FC286EA071FDDB26DF18F56DC7212
# Wed, 14 Feb 2024 23:33:10 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY39=https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe PY39_SHA256=FB3D0466F3754752CA7FD839A09FFE53375FF2C981279FD4BC23A005458F7F5D SWIFT=https://download.swift.org/swift-5.9.2-release/windows10/swift-5.9.2-RELEASE/swift-5.9.2-RELEASE-windows10.exe SWIFT_SHA256=D78A717551C78E824C9B74B0CFB1AD86060FC286EA071FDDB26DF18F56DC7212 VSB=https://aka.ms/vs/17/release/vs_buildtools.exe VSB_SHA256=D4E08524CB0E5BD061A24F507928D1CFB91DCE192C5E12ED964B8343FC4CDEDD
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Wed, 14 Feb 2024 23:33:13 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd40bdd80c4468ac7f308d2400156a72f5747c7cb69bdb7d4671accc0f47936`  
		Last Modified: Wed, 14 Feb 2024 23:33:54 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adad423e821e2962a0ed8fcaeef4fc5b6d264f4e233df1f5f4a70dc64e01406`  
		Last Modified: Wed, 14 Feb 2024 23:33:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126592b75536a5de779775360519ec7d954dd5cf5408daa77dd508021e40f312`  
		Last Modified: Wed, 14 Feb 2024 23:33:50 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6314ab08b2d7b9224b09b799022f7ce0ec0972654cd448c3530500ad18bfdf0e`  
		Last Modified: Wed, 14 Feb 2024 23:33:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fea7e437bbc4ef56d0c22b26318fe9e688861e38f52218e2d9143a0e2f5855`  
		Last Modified: Wed, 14 Feb 2024 23:33:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b81f9db4088e2b85452cdaf3ca6220201516de60776b09655655739373c144`  
		Last Modified: Wed, 14 Feb 2024 23:33:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ade9aef075dadc199a0f39b71c0b488e57427f034992b6cfe292f4d6c834ec`  
		Last Modified: Wed, 14 Feb 2024 23:34:25 GMT  
		Size: 150.4 MB (150367210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74d3e548df0b135992d78241cda7a96d72d3c6c925a1b2bf59f60af7a4c924`  
		Last Modified: Wed, 14 Feb 2024 23:33:40 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44412b74f8dfe193a7643fe43f5c6379b94cc703d9a24ead16c3d2188996f20a`  
		Last Modified: Wed, 14 Feb 2024 23:33:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad1c008256035f9149d9b198605819cd7a8a3aa52a57d0b4dd83c0f15e0005b`  
		Last Modified: Wed, 14 Feb 2024 23:33:51 GMT  
		Size: 47.8 MB (47800422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cd9d01b0365b5f9912922deade818995ebdbf757b3adc6334259c91f6ab3b6`  
		Last Modified: Wed, 14 Feb 2024 23:33:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0939cad9b503b6ac4764bac68878def7be4b2eaa2da382e4511f1792d86643f`  
		Last Modified: Wed, 14 Feb 2024 23:33:38 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e06a2f232a9e159e93122802e1925cda211922847e4a4d7d805bb8aa2cd1d`  
		Last Modified: Wed, 14 Feb 2024 23:38:24 GMT  
		Size: 1.7 GB (1650693533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12545ada71266bc1fd15fe83c3141e83c51aa78549d4199d7fc3224b6d84872`  
		Last Modified: Wed, 14 Feb 2024 23:33:36 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c5ac218edb3756b5a4ecb5080d34d65cd9efc54b208215740dd50033d5848`  
		Last Modified: Wed, 14 Feb 2024 23:33:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffa27080e3ec0f603a79b46d7354bcac076e542d2584318ac1c967d081615ba`  
		Last Modified: Wed, 14 Feb 2024 23:38:28 GMT  
		Size: 2.3 GB (2343615196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a7a78d65b7410f78309035ae006f59a8cc35004a6afa7527e9032b8ab37a01`  
		Last Modified: Wed, 14 Feb 2024 23:33:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
