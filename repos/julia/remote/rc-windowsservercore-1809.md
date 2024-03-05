## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:47fd8de5540166a51a7536003a0dbfc46541a25c138940b9d818b341da2e0810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull julia@sha256:f1dd42a0d23fe7eba9a2f3930bb4222abc366d74c522ae4da13571065d1d7db0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242210865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c476be14d6762387d1f4e2c526ea7409bad3b493a29069abf4a0fe8072364e2b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 19 Dec 2023 02:04:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 19 Dec 2023 02:04:03 GMT
ENV JULIA_VERSION=1.10.0-rc3
# Tue, 19 Dec 2023 02:04:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-rc3-win64.exe
# Tue, 19 Dec 2023 02:04:04 GMT
ENV JULIA_SHA256=eda5641debaec10195a448c1eceb8efb5b1b009a54eceb0bfebd85cc8f1951a8
# Tue, 19 Dec 2023 02:05:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 19 Dec 2023 02:05:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49f0cae5d4e90651e6bba403a8d205d3cf2c945c206177d952b99a01fcad8`  
		Last Modified: Tue, 19 Dec 2023 02:05:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0700b55cbaf873afeaca0021cffb58ad644a362ba0005e113e622d1a95fca68a`  
		Last Modified: Tue, 19 Dec 2023 02:05:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5a7b805831bce1b260a743e70888c877809110951fd4b0965d4823b346a696`  
		Last Modified: Tue, 19 Dec 2023 02:05:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f0c45df7b11a1ccd344c9894dc0ffb3586b62b1c6528322dbd531fab4cc4c3`  
		Last Modified: Tue, 19 Dec 2023 02:05:46 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9abb73af2c1ce8a942f7e970d321657764e50dadabddc30f1a2f2492b240ad`  
		Last Modified: Tue, 19 Dec 2023 02:06:10 GMT  
		Size: 182.5 MB (182495360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327ded4626ad278ff724690303e93a88151d2fd8b30621ad5e51c9360b0c817`  
		Last Modified: Tue, 19 Dec 2023 02:05:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
