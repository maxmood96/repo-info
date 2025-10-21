## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3f33be8fe9e3496a9e954d3af5f3466caf3201d9c8c009df451489829551d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
