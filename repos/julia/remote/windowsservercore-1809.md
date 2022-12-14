## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:e8e4f29e0a4d275e53fe32b4c9a2561bea969bc2e9b97608e948157bc4bd009c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull julia@sha256:3b2d8578e9586a67ca0c5bd250fb87be38c34088a087f5f571a5eb98e2e4a464
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2922873333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1331ead9623cdce57c2c340b709044dc07efc6f09ac34e3a0adf5c6337fca81`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Tue, 13 Dec 2022 22:48:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 03:46:29 GMT
ENV JULIA_VERSION=1.8.3
# Wed, 14 Dec 2022 03:46:30 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.3-win64.exe
# Wed, 14 Dec 2022 03:46:31 GMT
ENV JULIA_SHA256=1e5cc98bf83028809f6e37d205df660e3fb27d35e95c88944c1106a6710cd909
# Wed, 14 Dec 2022 03:49:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:49:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc9debb9503ac53c2f64685982eca56ac5110ea6baf7278b27af54ab8fbc409`  
		Last Modified: Tue, 13 Dec 2022 23:54:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512d58e03040f95b924f3a5fe0d262d5bdb1f8776cd43a829ff03d737366d5c`  
		Last Modified: Wed, 14 Dec 2022 03:58:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1804577820fec7894ae9cca21130f1826c4662e23068a11ac79c9124a798ece8`  
		Last Modified: Wed, 14 Dec 2022 03:58:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7033f5e32ee2b4a345872f49ec2b3180103df998668ad9b3b407aca884d7d9`  
		Last Modified: Wed, 14 Dec 2022 03:58:13 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8e67e701fba0b89e4f262fa9d8c7f956f8612ee680ee177a3ace791eb07981`  
		Last Modified: Wed, 14 Dec 2022 03:58:53 GMT  
		Size: 142.2 MB (142169012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71061191b45bfc46d6e9746bbd5fb6d5cc4870cdb69c7a2ae46873c796ac3a66`  
		Last Modified: Wed, 14 Dec 2022 03:58:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
