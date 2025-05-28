## `hylang:1-python3.14-rc-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:18fec0d669deb58b8d0083d22249f35b3c1c32663673d7e233958a544a573df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:30ebcb9760fd8a132bbe34514f52747d70135913579d5befc259a1252fcd3884
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2343136213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d22e1bac7bf2f2f6ccdb5121078fb06d0483e9c10bfcadac3d8b828b9255a71`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Tue, 27 May 2025 19:14:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:14:30 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:14:31 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:14:32 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:15:32 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:15:33 GMT
CMD ["python"]
# Tue, 27 May 2025 20:21:21 GMT
ENV HY_VERSION=1.1.0
# Tue, 27 May 2025 20:21:22 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 27 May 2025 20:21:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 27 May 2025 20:21:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bae92a971aef15b45a0fe18763259990b4ea36ffe686528e6fd4923a8010e90`  
		Last Modified: Tue, 27 May 2025 19:15:37 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8352cb1e0e88c3078a0a72be592c7edc94e3f3253ff6ec46bcafb4ef9038ed`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3b2ccd9d0ac90fadc17a7086116791be7b8335eb2cfad4da0e070208dd08c9`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feaec92c690bce384e65977ad738d1ae9b2a73577c5300a64accaf927073b24`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee323e7444772ea2d2e2e1b51a5f2ccf0fca60470a8d413b72350e5f794de22`  
		Last Modified: Tue, 27 May 2025 19:15:41 GMT  
		Size: 61.0 MB (61003907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3762902937236a108e91436aeee2b73051dbe1c073e0de1f10fafcfe775221`  
		Last Modified: Tue, 27 May 2025 19:15:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5696d71d0e5105b494178f5947b2df0afb128d18b0507c0fad782b786ba63fdf`  
		Last Modified: Tue, 27 May 2025 20:21:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6285a0c454cf4a502e814793be07c869e4f358f4f0c9b0010c07265fde585789`  
		Last Modified: Tue, 27 May 2025 20:21:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e74ff00a98affd1ca4bacbb6530194c49914cb04be028a0ec16c97900d3c3e`  
		Last Modified: Tue, 27 May 2025 20:22:00 GMT  
		Size: 8.5 MB (8493780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759750ec5e764c7fff83668c1fce903db967cbd7e918d4c70775fe0461321cbf`  
		Last Modified: Tue, 27 May 2025 20:21:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
