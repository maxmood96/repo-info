## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5fd1868d86561aa17af59a1e11e12506c7e878876203b80d7bf14403049271b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:18959ef74700387208586af4b46e532357b4581331ad953361cea92af168fde2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2546753259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262545211bfd4cea8724fad690d4ab93ea55cd46090b39947096578dd865c03`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:44:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:44:32 GMT
ENV JULIA_VERSION=1.11.2
# Tue, 14 Jan 2025 23:44:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Tue, 14 Jan 2025 23:44:34 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Tue, 14 Jan 2025 23:45:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:45:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e2e9d70b5503843673c823b610a83d3dd3b4a0be46c1ddfe38bf6ba47d843c`  
		Last Modified: Tue, 14 Jan 2025 23:45:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb92cfcc5a2790a46df3298ea3aa9f01191d0d0b4082b8187c35cb6672fa85`  
		Last Modified: Tue, 14 Jan 2025 23:45:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01b1ebbd33b844772197c48dd6f4bf395845a283d1421213e161d7ed7cf4ce3`  
		Last Modified: Tue, 14 Jan 2025 23:45:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ddab2ce6bca5d2d83208f4abe5e14679c7fa1c95706dc0b4ba84d3e16a6b3d`  
		Last Modified: Tue, 14 Jan 2025 23:45:57 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708fd212d26923b8214b201f2a4835063e3ca1633fb9eda8efd1b362bd05cc5`  
		Last Modified: Tue, 14 Jan 2025 23:46:32 GMT  
		Size: 284.4 MB (284361585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a39a5a5b254f497e4c4d58fc8f2775b6d19fa4a88f232754c5cc742f607998`  
		Last Modified: Tue, 14 Jan 2025 23:45:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
