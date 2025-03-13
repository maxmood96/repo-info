## `hylang:1-python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:15c6eb6329b629bdec29f04ed9925313895c247c7dbbc0ea5a10fa17bfa28b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `hylang:1-python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hylang@sha256:05f33fe94f9065f88da6f8afa2ace27e2a0ec275cfc57ed6640b3cc50a0f2a39
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338410047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c042bc0449f4e17c17c373ea910344de2c0a65c4e39a70ee262a7ea4adcf8`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:54:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:54:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 12 Mar 2025 18:54:45 GMT
ENV PYTHON_VERSION=3.12.9
# Wed, 12 Mar 2025 18:54:46 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Wed, 12 Mar 2025 18:55:31 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:55:32 GMT
CMD ["python"]
# Wed, 12 Mar 2025 19:21:19 GMT
ENV HY_VERSION=1.0.0
# Wed, 12 Mar 2025 19:21:20 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 12 Mar 2025 19:21:57 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 12 Mar 2025 19:21:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2992cfee4a8a03d26a5f52f0f69acafa648b5757d143d21d98522c887d07c449`  
		Last Modified: Wed, 12 Mar 2025 18:55:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f331a3ba5eb9785c558490c986f306f28f3c3385ccac3752b4f053e583a253d`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246785186c2ea9d38a2bf7766b1f0a19c5803bb00b953725e1ac7fa17a9aae27`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdedecadbaca5b44e37bb50483c44e212efc7b64b5251ddc36c1286354285d3`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a043e0a111b1a6b32380df89edc23d32c905c60a14e37372bc9f0088e28e35`  
		Last Modified: Wed, 12 Mar 2025 18:55:39 GMT  
		Size: 59.9 MB (59941957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980de137b96e235773fb475806933aec82fb16e19a7a5b5193ff374c70372e4c`  
		Last Modified: Wed, 12 Mar 2025 18:55:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb325f3a401ce123cb8cbaac1d3050b1e06e950d1636121779f6728ac55a2536`  
		Last Modified: Wed, 12 Mar 2025 19:22:01 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492e36f517c11d3d7400197e3021261f46767b2dfcaaee42715cc0a095b3ae7c`  
		Last Modified: Wed, 12 Mar 2025 19:22:01 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f97a6e794cf60a808ad565166a4570354b8056a2ee479bbd43bd62c3bdaf6`  
		Last Modified: Wed, 12 Mar 2025 19:22:02 GMT  
		Size: 8.5 MB (8516531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf7b5a379f87e17b3d651c9a2e062aec068918609a70c13842092f60a6a4001`  
		Last Modified: Wed, 12 Mar 2025 19:22:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
