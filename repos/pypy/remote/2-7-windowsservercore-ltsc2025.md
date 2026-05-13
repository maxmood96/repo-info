## `pypy:2-7-windowsservercore-ltsc2025`

```console
$ docker pull pypy@sha256:0063a4234d3b54e74d3ce37ad34cc5559891ec83c4a10c22e552a27397a3289c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `pypy:2-7-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull pypy@sha256:0a7d5201c43df6741348f272a40b2272b5b358386701dd508962d807ef41b317
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2247226568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f68166eacc813528b11abbb398524a56e3d10a14f1f40497aa14bf6769024b5`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:49:59 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:50:05 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:14 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:15 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 12 May 2026 23:50:50 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '43cf8c09e166ca53d4b54c8d99ab0ad29df43b980cae53ad954c2a3a5e2eb056'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:51 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f067daf25dd6f577b7a9808d0a4465eb0cf8ee508d20eacffa1b05dd949f8`  
		Last Modified: Tue, 12 May 2026 23:40:55 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0479c64e69c3a8f57d2d3d6cf99253b4c2b8a2403761bf36d4d9e3834601cd5`  
		Last Modified: Tue, 12 May 2026 23:50:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb402df59d7c9202ac70bfa4d4f9a2a91fe435188f8ee4002a23fd69c5829bab`  
		Last Modified: Tue, 12 May 2026 23:50:56 GMT  
		Size: 381.3 KB (381290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab0bd7861c0be4d014bf6333aaac4520bf95c17938cbaf127f790f2266de71c`  
		Last Modified: Tue, 12 May 2026 23:51:00 GMT  
		Size: 15.6 MB (15559792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503b87a9aba152ef1d31fe4c25a583b14b4e70726161ac359d9cff462a6934d5`  
		Last Modified: Tue, 12 May 2026 23:50:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b4648f9dc629d1d2370e607c3e9e78320abaa63f3744ee1ea91d0296bd1bbf`  
		Last Modified: Tue, 12 May 2026 23:51:00 GMT  
		Size: 25.3 MB (25338278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788ead1ee610fe4693447a54dae16a66cdb90342930024784db1987ff01af82d`  
		Last Modified: Tue, 12 May 2026 23:50:56 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
