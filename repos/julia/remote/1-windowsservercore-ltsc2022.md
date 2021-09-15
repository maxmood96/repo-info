## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4096ca9d714e12412fca2afc6238101d1d5dce3c96dced705cf7b7c1fb503f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull julia@sha256:ebe312c101cdc0446f0100d8958b99782871320c3dc849a81f33535310f6d3c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258598379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccc1559a12b6e87b0bc7f13640115d1d8959283cd5e9cd6f3fbc1b1bae26bdd`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 13 Sep 2021 07:01:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Sep 2021 12:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 15:16:19 GMT
ENV JULIA_VERSION=1.6.2
# Wed, 15 Sep 2021 15:16:20 GMT
ENV JULIA_SHA256=380115d80e2f0bebe1885b80f67cf9330b659722f50608495962ab3a00e02977
# Wed, 15 Sep 2021 15:17:29 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 15 Sep 2021 15:17:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:48a76b150a3a1ee8efbc87797c38de66d24a71421fce2754695fed8227d4cc3f`  
		Size: 873.2 MB (873175411 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3fda9a0667b0cb96fa50df6568908c70087df9372ac60c91c1ba417787ee1faf`  
		Last Modified: Wed, 15 Sep 2021 12:59:54 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720dbb9b25d9f567cbedc81fe71079519831351bad523c01a6279b13b279a34`  
		Last Modified: Wed, 15 Sep 2021 15:33:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbc3f4ba4e819fb3b2e98bb704bdf16cee5cbd0c7ae492b5710ae04f5cd9767`  
		Last Modified: Wed, 15 Sep 2021 15:33:21 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d0f9bad9241940f86a2aa6c6f1f29c0a2ab691b4a0bd9205afdd1c0558bd23`  
		Last Modified: Wed, 15 Sep 2021 15:33:52 GMT  
		Size: 133.7 MB (133718589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaee49c223b2b05bf4be2194612fb0db442e9318175f4ca2c957a54dcf627e2f`  
		Last Modified: Wed, 15 Sep 2021 15:33:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
