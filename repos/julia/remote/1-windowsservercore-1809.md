## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:d21f77a65c16a3c54eedd95b8bbf900382f6227a12fdcf1c8c4da162320023d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:9941efb5ae7a9bdfcae171c75372bace337cf9b67077e582f8ff90f6f8e9781b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263572003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3256b9f057b43183193ad3039b1966f6990a6950ed81d7bb1d5a58dffb35731e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:58:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:58:47 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 14 Feb 2024 19:58:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-win64.exe
# Wed, 14 Feb 2024 19:58:48 GMT
ENV JULIA_SHA256=f58aaa631748a5b0389586f3a3b7a081a2a6ac219a5a73a501ac61c0d99daebd
# Wed, 14 Feb 2024 20:00:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:00:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63f2b6b5f89b008d7b63ceafa85d217a258c84d2ed8f8a38a0cd3060967e6f`  
		Last Modified: Wed, 14 Feb 2024 20:00:30 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96994fba50f8940d1a3854f28a22ae8e6639193ae8a89af2c8298eca14d9e0c9`  
		Last Modified: Wed, 14 Feb 2024 20:00:28 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f880ce82a32f3b9fbd4d867db9141b549899f5fb91151a0bdead8de7f0bef5`  
		Last Modified: Wed, 14 Feb 2024 20:00:28 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df397a1a717473c6a35ab39292dd21179cbdc92a68b2c916612a4b1f704ef099`  
		Last Modified: Wed, 14 Feb 2024 20:00:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956b1a236dd8ea09edc512ceccbbb6ef656e5f0bfa2a47191dfb015895c560b7`  
		Last Modified: Wed, 14 Feb 2024 20:00:53 GMT  
		Size: 183.1 MB (183116344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fac9596bc36033630fd5dbd38b409866576945d4758ff06ad69951a20c3403`  
		Last Modified: Wed, 14 Feb 2024 20:00:28 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
