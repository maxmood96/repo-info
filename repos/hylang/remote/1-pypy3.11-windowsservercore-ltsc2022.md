## `hylang:1-pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:2f379617096953940df1d56659f4abcd6c35f51439ad7b0dd4d02435e88937f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `hylang:1-pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull hylang@sha256:863b6327bd4d57866008d2b70c101012afb14d164a4d2dedf27045d15241880f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336070266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8dffde1dfdd3062b1473a354e75f50428fe5a085da10bf714ccaeaf159d9e1`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:59:11 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:59:20 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:59:20 GMT
ENV PYPY_VERSION=7.3.20
# Wed, 10 Sep 2025 21:59:59 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:59:59 GMT
CMD ["pypy"]
# Wed, 10 Sep 2025 22:22:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 10 Sep 2025 22:22:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 10 Sep 2025 22:23:26 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Sep 2025 22:23:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e206e7786d2e85b306264f28d937329bc1c3abb6dea87bf713a3107950124ae`  
		Last Modified: Wed, 10 Sep 2025 21:55:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16296a6ccddd8393882a36c66227440bad609c6ed9878ed96ebe45e5fd83e26a`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 347.6 KB (347646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e1e55467d873b816a64df3e99fc89db4af8f89db26e2c738db969eb09bd99c`  
		Last Modified: Wed, 10 Sep 2025 22:00:31 GMT  
		Size: 15.5 MB (15526937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cdc42c67473c462d81ae0c2788cf3a132e8d4ceab129a17f3f04f937208bd6`  
		Last Modified: Wed, 10 Sep 2025 22:00:31 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b029167fd7a3956a7a0e24eef14cc373ff8581c69cf8de6667446e07fde2ca9`  
		Last Modified: Wed, 10 Sep 2025 22:00:33 GMT  
		Size: 30.7 MB (30671963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77232253b6dfd7a25a264a2aa48daed52310d918b93e8284f64982b06e33e57b`  
		Last Modified: Wed, 10 Sep 2025 22:00:31 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fafbe117f25ef670f124f832add2fccf5fa577eef2f2998aa74186eaca08af9`  
		Last Modified: Wed, 10 Sep 2025 22:23:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc4235b73cb582702a0f72d5b15199e6c515f7f8169c248529721d1e273924a`  
		Last Modified: Wed, 10 Sep 2025 22:23:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4e0fb503d513122aded7518bbdbae898970c5cca5e85d40813e2eb23f249fe`  
		Last Modified: Wed, 10 Sep 2025 22:23:43 GMT  
		Size: 7.4 MB (7370875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97a1ac8e238273ef51156d0af52823d5d6b5d14bdccccb51859fbcd0336f0bf`  
		Last Modified: Wed, 10 Sep 2025 22:23:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
