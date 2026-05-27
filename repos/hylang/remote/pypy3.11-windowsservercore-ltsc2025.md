## `hylang:pypy3.11-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:200e92f8a8ccb3d5e91a10bd1503243cbe6bd7180d5cdb9e9e6561bcf3fe77bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:f835cc508c923ac7f69a820dca6a84f428f5b31076d7f7b12e7b4d94ae5e2c74
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2260904533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b98302b52129b36b55c4a46dcbbd2a09877175bbf75ad6bc187b57cb60edc76`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:01 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:11 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:11 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 12 May 2026 23:50:52 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:54 GMT
CMD ["pypy"]
# Wed, 27 May 2026 00:15:04 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:15:04 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:15:57 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 27 May 2026 00:15:57 GMT
CMD ["hy"]
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
	-	`sha256:d4498f1426c9298e6d204f6b74e5060c8b3bfb19e1328586b50b0bc0e9976829`  
		Last Modified: Tue, 12 May 2026 23:39:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88aaf7366d7bfe93d451122f3a8944fbae359f4736d40dc0fafee059a6158b43`  
		Last Modified: Tue, 12 May 2026 23:50:59 GMT  
		Size: 379.3 KB (379332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3026da7f27048853cc7e42b4ab25545ac90ec5c11d200a46b4bdc72d0b5ecf93`  
		Last Modified: Tue, 12 May 2026 23:51:04 GMT  
		Size: 15.6 MB (15559740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037c75ceed8a7791f76d2e136f20af3b0def5ba22cf6bc6559d0d6ea7835b5fe`  
		Last Modified: Tue, 12 May 2026 23:50:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cfd80338a499acab2bc1bab0a354e8d9e82c6b841f0a1548242f2adc3f4835`  
		Last Modified: Tue, 12 May 2026 23:51:03 GMT  
		Size: 30.9 MB (30932210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0ca5fe4e0cceeeb28c22eda5846c5cc99e3a968bd7dabc234bc0d05a1c444d`  
		Last Modified: Tue, 12 May 2026 23:50:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538cafec45cc5610a19568d24de1664b07401a87828d99b2a34ac2de410cb6d`  
		Last Modified: Wed, 27 May 2026 00:16:01 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41970be7d2f5bb774f1f20a5093277932b0eacf110d7f22db1d2ed3c3eb2f977`  
		Last Modified: Wed, 27 May 2026 00:16:01 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badf1ba9788e50142fc3d5f683be476a95d1921ef050f198cf987cab3c401b2b`  
		Last Modified: Wed, 27 May 2026 00:16:03 GMT  
		Size: 8.1 MB (8083509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f87bfd489017a9d7414065d25c8ed4e55a0f89a7c96771feca0c91690c698d`  
		Last Modified: Wed, 27 May 2026 00:16:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
