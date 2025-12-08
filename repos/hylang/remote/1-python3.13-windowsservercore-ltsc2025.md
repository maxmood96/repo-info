## `hylang:1-python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:bc052e4bf4944693b059dfc60855d3ad844489703b23179c4079832ed702e472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `hylang:1-python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:3c87fb3c0047529e45ac99f506eadbdc4581a8320560ff75a2eb249fbcb0546f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3302719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2937ca095266cd706f7ad8caaffbbb81fc39ce0b31fc449e9ce694423925741f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 01:08:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:08:52 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:08:52 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:08:53 GMT
ENV PYTHON_SHA256=ab30cd76655c6c91243b4f4d5a8499020f6503aa58e92b3e2e94ae4af7353257
# Wed, 03 Dec 2025 01:10:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:10:47 GMT
CMD ["python"]
# Wed, 03 Dec 2025 02:13:34 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:13:35 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:14:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 03 Dec 2025 02:14:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc79475b321f3f485f171323886acb82a816c3ca538395f80d4f20cc7d23978e`  
		Last Modified: Wed, 03 Dec 2025 01:25:20 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c820b1100bd9cd0766e6c92e5ce9d58649e89891538731b04492f07df33cba`  
		Last Modified: Wed, 03 Dec 2025 01:25:18 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791801f468282f6fdee8125777a9cde8a86850e23b6d9da874f0e7ca19283600`  
		Last Modified: Wed, 03 Dec 2025 01:25:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b374fa80ecbd3d52db3cf2c01e239bf07e2b64c9f5ef485795031b0b3181e1`  
		Last Modified: Wed, 03 Dec 2025 01:25:19 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a348876e947f4a980da4f96cb2d23ee574fdeab878abf635616422689c9421`  
		Last Modified: Wed, 03 Dec 2025 01:25:36 GMT  
		Size: 58.8 MB (58789330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009e6fdde1baeec39614d9adec7183acc94c93666c4ca6b4361eba9bc4208296`  
		Last Modified: Wed, 03 Dec 2025 01:25:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af48061016506245c2b05d9e012d18b10a69d252078912355e570c5ea6ce769a`  
		Last Modified: Wed, 03 Dec 2025 02:14:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb71ce64fcf283646731aee3b0cc94bf9923ae9a3f7868f7f3a320fc00c35891`  
		Last Modified: Wed, 03 Dec 2025 02:14:20 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539432d8a2d9bd24823cbfdba5b1a8ca92008c95060c3a3b30a6aa2c087cfa66`  
		Last Modified: Wed, 03 Dec 2025 02:14:21 GMT  
		Size: 8.5 MB (8463506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e20e383cc2db01baf3ab9d6a4ee15c5928755944d61231757f2830a4cc656b`  
		Last Modified: Wed, 03 Dec 2025 02:14:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
