## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:54468380ef6364f9e8298371c6135abf0d99e3bf53a09c9f1308cdcad343f8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:710c5d609bc83bb05746cae905def34f1e9ff8d83ff4f83a8adda4b9f35001c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3545626674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb390f2895272452331b1b1d20010368e5385cac0eb7813535828ddf50f09dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 19:01:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 19:01:22 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 02 Dec 2025 19:01:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-alpha2-win64.exe
# Tue, 02 Dec 2025 19:01:24 GMT
ENV JULIA_SHA256=ec84bd651c739436b2ab397f4a156ed269030f277d075031104eecbf6904079a
# Tue, 02 Dec 2025 19:03:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 02 Dec 2025 19:03:26 GMT
CMD ["julia"]
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
	-	`sha256:8141b58e228ac47c42461930c677cd23e8e308c83fed29a5847b300cc7b1e828`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f4cd6912772159706904dabb489e9f38f4fcbdc4ff08bfaec1c0d6fd3ac3d4`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdde5cf68e32bec7badd008412379831c34f31083a038f8d79aafb23d6d121c`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88ed419ff80e5f510f8953c401d8c9d63ac2734d43c164fab3d9475f01457d9`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff8814e2bdc25e8c91396e45b0d6c3af22d179237537ed881bc9fdacd45ffb`  
		Last Modified: Tue, 02 Dec 2025 21:03:26 GMT  
		Size: 310.2 MB (310164340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8fe5a9bde1fcf9fcb2c9164dbf68054c011dc27998fa5b7cfb5d46dd5d5ce`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
