## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:096ec1ac6bd7714f5cb4555a0f63af46ee152de56046f33fa46583ca3c4b278e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:802388f92d0bbf7255a137144f8585c9a803acda8bc42a2a6b64d3985d3c3635
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3173800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275b2acd98b73751584d6ab08bef0cd0d9244e704d549922417a67a3f9fbfcb4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 19:18:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:18:03 GMT
ENV JULIA_VERSION=1.11.4
# Wed, 12 Mar 2025 19:18:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Wed, 12 Mar 2025 19:18:06 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Wed, 12 Mar 2025 19:19:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:19:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf90ec15b3a941bc20ef48f0154930ca08ce03265e5168e2c0a92959707e2638`  
		Last Modified: Wed, 12 Mar 2025 19:19:20 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519faccc1c0f6bbe5ec6c3ece84b08c63c60e549ee7b9945b97b31113fd4f424`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed31a36ee885bb4b3c52be3375f3efe98db930128da96d83fbf16b62fa4b320`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152e6b3c43529daecbb6aafe1d0a99d66d2c00fe01b903d09ac45346f7d92b09`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aef7aab92ed9cda3aea0d70ff5582a0e70a3c1ec10b1e0b80383b4732a6876`  
		Last Modified: Wed, 12 Mar 2025 19:19:59 GMT  
		Size: 265.1 MB (265146357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582dbe2668383dc1384492860b44d52092aa598848ef0aab775074836e7da1f0`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
