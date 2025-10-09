## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:86957bc28b8cbc3c9df766b39ba1f643f57055b89c1e34c9f87f1c110ba899ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
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
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
