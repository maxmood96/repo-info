## `hylang:windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:e03757d13ba34b550a0ca4b11356f7f4f80f9427a559ea0357ef924faf0a9ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `hylang:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:ea6cec9be63d6ab85dadcbcd594af90c58278964b58d651703bf4ebe88b79e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3304767565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61db573fc9904ffa048486f9c7f07e3de54b2f8c189f0c16e06af7473f028e64`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:27:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Nov 2025 19:27:17 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 11 Nov 2025 19:27:17 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Tue, 11 Nov 2025 19:27:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:28:00 GMT
CMD ["python"]
# Tue, 11 Nov 2025 20:16:24 GMT
ENV HY_VERSION=1.1.0
# Tue, 11 Nov 2025 20:16:24 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 11 Nov 2025 20:16:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 11 Nov 2025 20:16:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f250670b758b44e95ad84456ecd30b7bdfa180b65c53a34d483a5ba0c756999`  
		Last Modified: Tue, 11 Nov 2025 19:28:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c3f1b6f0981fda4e4a9befb9c5eb4328d1a56d1d15be4039f05bc04ba6ad4a`  
		Last Modified: Tue, 11 Nov 2025 19:28:16 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14206655eb51cd8f7e11f511e14c9de42e6d11683fef738a6822dd46b126886e`  
		Last Modified: Tue, 11 Nov 2025 19:28:16 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a8611e54ad3ef409b3c1abc766302f99cbfef3cd1d31d66e68e11a3e28fac1`  
		Last Modified: Tue, 11 Nov 2025 19:28:23 GMT  
		Size: 60.7 MB (60747574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911cd32975f839ab524d385bc8995e72cab2a192367a8d5e638d613be3b5ddb`  
		Last Modified: Tue, 11 Nov 2025 19:28:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b553b209eb204ab7468c306540896b765864abbcfd3e0edd02f3b64fe55071`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5e4fde50b34c7adb2c418fbdd955002095e9172b42fc9aad75a9b89fdf7575`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b7cc51457e745228d3b699024febdeab0e81e47e70e17b8b68691b4c25811e`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 8.6 MB (8553717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabde63a39d70ad3aa13a6a1a3536caf7a6a68b23d3f4150498f7a507cdfcd47`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
