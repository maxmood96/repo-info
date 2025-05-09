## `hylang:1-pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:ddf4fa771b4965960855277455cd6be681025289c5b1a3270aea5ee51e687e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `hylang:1-pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:d9bc3b6ec4bd31f3bb58e486baaf92f598ce204a35ab2a890768807012f225f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327463830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8852be3a9fb64ad207e02b4ede06bca81cb061fcbcf65365eb82bd276d62f0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:27:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:28:03 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:16 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:17 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:28:50 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:51 GMT
CMD ["pypy"]
# Fri, 09 May 2025 17:31:34 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:31:35 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:33:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:33:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6e63c5ed26e532f8ba4909314a1ceea6a7fc0164e873d9f3f4162d2b3e699`  
		Last Modified: Fri, 18 Apr 2025 03:28:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fdb41e48d7c7cd86a2fb751c554d1017f2cf44f5fc6d06595a028866793723`  
		Last Modified: Fri, 18 Apr 2025 03:28:55 GMT  
		Size: 345.1 KB (345074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07f139d4c1a7b65454d5dbc5551b814fd3028925122191633d0c9eb9e7aabe`  
		Last Modified: Fri, 18 Apr 2025 03:28:56 GMT  
		Size: 15.5 MB (15529087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a9a1ca262dc9b62bf08c772bd5bb9cf19886ea4489ae0468311ca847d09d8d`  
		Last Modified: Fri, 18 Apr 2025 03:28:55 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bced1212c91ac5cbc7270542793c5b67f1cbbe0b10fcfa6ef5361076f936adb7`  
		Last Modified: Fri, 18 Apr 2025 03:28:59 GMT  
		Size: 30.6 MB (30619211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3312b4cbe080da21260b1cb85f95a2ade9737fe408899d5a16eedf5ccbcd6`  
		Last Modified: Fri, 18 Apr 2025 03:28:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079b3d00631129609f4e2a3de6eb46f02dd49c5f084bf4565ac01f4f6012da15`  
		Last Modified: Fri, 09 May 2025 17:33:20 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26e0b9801cd6cb811a1a0b038ddda89b0d166c5cd719b0a07fb343a004a8b`  
		Last Modified: Fri, 09 May 2025 17:33:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f89c9a280e29ac7e5ace5211368862bedf2f1433f21c25046cbdf55b2e2f4a`  
		Last Modified: Fri, 09 May 2025 17:33:21 GMT  
		Size: 7.4 MB (7380171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de36629c132c209b80d28127f66a549f2f6825bb6ac59b6a42b43aa7ce9c9fe9`  
		Last Modified: Fri, 09 May 2025 17:33:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
