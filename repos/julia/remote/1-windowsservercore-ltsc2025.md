## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:000287370167255970e6676036cff52dd994b6da1d49ac564abd6fdc329e4c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull julia@sha256:099007ba34c82607228b74220952891f8c7ae74ca811435f58f3b307c3c45e38
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3777143149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b179accfd8c9d2b92e94b3b0d0abba0be682a4ead138d883062e2c12fe02`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:42:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:42:41 GMT
ENV JULIA_VERSION=1.11.6
# Fri, 11 Jul 2025 23:42:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Fri, 11 Jul 2025 23:42:43 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Fri, 11 Jul 2025 23:43:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 11 Jul 2025 23:43:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44189aed01e051f91d7990e8be705a7f7695f29a85c36281685d6da49c697c58`  
		Last Modified: Fri, 11 Jul 2025 23:47:28 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb1b53d38844f3b07a14d0c5cb89e6b043ba810ff2dd2f0241d5a49bdb170db`  
		Last Modified: Fri, 11 Jul 2025 23:47:28 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a6edc458acb58f1ab2c5f6bc83c2442a4e37c8508495a3d9ba444f15f72d2`  
		Last Modified: Fri, 11 Jul 2025 23:47:28 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32ea01606b0d7f2a87c7016d0b3f7913fc3af3862d19acf8b2c84f2b814c1c0`  
		Last Modified: Fri, 11 Jul 2025 23:47:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2956eeb5b7d54ee10a4965af81feec4b5311bf11da8ab805d130862beb54a0ea`  
		Last Modified: Sat, 12 Jul 2025 02:03:42 GMT  
		Size: 286.0 MB (285963100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25e045427066ebf42103f2b5ed510236603390fcf0ead4dcda9e67924b4047`  
		Last Modified: Fri, 11 Jul 2025 23:47:28 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
