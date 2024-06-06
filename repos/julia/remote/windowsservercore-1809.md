## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:c64695a38984d78a040b22c8f1fb4ffcfa0557e04e2b488e58735260c1de72ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull julia@sha256:59ba3e0a27293aea4275ec561bc3b2de33a117e34f55e1d181339e9ba0effb15
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2367167698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394c000cc22352ebdd258f02b1cad9be87c7d121077eaa9fba827924f73e388d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 06 Jun 2024 00:56:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Jun 2024 00:56:23 GMT
ENV JULIA_VERSION=1.10.4
# Thu, 06 Jun 2024 00:56:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.4-win64.exe
# Thu, 06 Jun 2024 00:56:24 GMT
ENV JULIA_SHA256=c1b659abc90991dcbdf461f33cae483501da736fc223c11d4c51f337338ccb21
# Thu, 06 Jun 2024 00:59:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 06 Jun 2024 00:59:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2238fe9faf15f770b72f6f0e3ae0420de2b15aa689f8021884cfef7597952f5`  
		Last Modified: Thu, 06 Jun 2024 00:59:07 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c3a72f3721ea0aa69147ca567a6009e17e871219c4a521f8d7e772e957a478`  
		Last Modified: Thu, 06 Jun 2024 00:59:06 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ba643f6f5f571a0efe7097f64b350ce04c1cb90eadd2ae2891ed6f17c70d1b`  
		Last Modified: Thu, 06 Jun 2024 00:59:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975b02e8ddb3eded154a838fd8f1094545c5acd029081c6417f2bf4b024029a4`  
		Last Modified: Thu, 06 Jun 2024 00:59:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0601c38ec0f73184e867807e167c4adb84c81f779229ba77de0dbb9de37c5085`  
		Last Modified: Thu, 06 Jun 2024 00:59:29 GMT  
		Size: 187.4 MB (187449735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06a47c35ed7cac482cfa1b571a753fa0a63ba1ac546d1c969cf1943e07f0b15`  
		Last Modified: Thu, 06 Jun 2024 00:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
