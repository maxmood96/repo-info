## `hylang:pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:393b6c08ebbe3ed71dc4dff16e4c9b740cc945e52bb64207af6a2fbc6a74b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull hylang@sha256:0ba9ab9d5ee202ffcb3f23d21991b8325c54bb546971fef056c9b434ff56c258
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1542976089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b47c1ef145e88e41769f4630b3e821b4fb65c7d01db34a50b9ba4d38403d439`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:51:10 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:20 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:20 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 14 Oct 2025 20:51:59 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:52:00 GMT
CMD ["pypy"]
# Tue, 14 Oct 2025 21:15:55 GMT
ENV HY_VERSION=1.1.0
# Tue, 14 Oct 2025 21:15:55 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 14 Oct 2025 21:16:40 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Oct 2025 21:16:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06017d8dfd283d3ba640a46147e5bf79140a84f42c8163da89fe2d9369a9cce7`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 361.5 KB (361509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4983d91b47c66e46c468fe23f65722c36e054b5809d1d0d4f7d3ad015df56fce`  
		Last Modified: Tue, 14 Oct 2025 20:52:16 GMT  
		Size: 15.5 MB (15538662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda269244f492062ac2042e6281c03e7f29ab22a349b3739a8a5260b9e5dc79e`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9274475d419b3c61456c76ce808a22db431c6d0d3a0f1c8def121d17495b18`  
		Last Modified: Tue, 14 Oct 2025 20:52:18 GMT  
		Size: 30.7 MB (30674033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2860984c75ce0d6c23fb3b1b152d8b1ae57265a4779973b86586eca927dd13`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10ec2a8c8c0b132e64600a3b2118c460d49735b75931887ed0b2d6ffdf28ab6`  
		Last Modified: Tue, 14 Oct 2025 21:58:29 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b772bd1ea80d1fff3a85af85cb0b42eb1ed89ea904cf9d2749e7b6b33c3e169`  
		Last Modified: Tue, 14 Oct 2025 21:58:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76837461917bf8121ac5fc48223c0e80469d696ec5d5850198291d324a281009`  
		Last Modified: Tue, 14 Oct 2025 23:17:47 GMT  
		Size: 7.4 MB (7374877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d4e53cd7fe4351330a6b9a1e7f2d7369bd67612e5bf04d6a7bb994497ceaad`  
		Last Modified: Tue, 14 Oct 2025 21:58:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
