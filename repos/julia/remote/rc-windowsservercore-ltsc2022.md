## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:3c239f3ea36c8b430fcc90ca5997ffd002aceffb0d0e8f3fe68fa08eb9cd32d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull julia@sha256:401ad7585973d604032c1b9799a9a1fb852ed7811ab8526b4f38bcac9284c4ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2382523826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd18ce4a7e34a140a51c9b47b6d839f2eceaa1977ef7d0322f4d02a12204d02`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Fri, 01 May 2026 06:34:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 01 May 2026 06:34:35 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 01 May 2026 06:34:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Fri, 01 May 2026 06:34:36 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Fri, 01 May 2026 06:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 01 May 2026 06:35:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77be2f9c243b0e263c88ca2d726022040687be630dcf57393cc6b22b4185dbf`  
		Last Modified: Fri, 01 May 2026 06:36:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e932476babec9ee83f5a230f626301da45f76fac5cf900af2c2648cbfc2b5a`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a7358644a33dd8cff75bc9310d43243c6391a7112dcf15fd1ef85c3047e72`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c14313f3dab02546408316191117d691fb0555f1bd46b60e37b44f496717d5`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383535af7e630d3f2db2832c2c8e141e0298958ab5dba981083f1c8091e4fe7d`  
		Last Modified: Fri, 01 May 2026 06:36:42 GMT  
		Size: 312.3 MB (312306104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3752c15d2e0e0040ccb2d4d90be4c5a921452d943fc6793c3f1336a82bc4f90`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
