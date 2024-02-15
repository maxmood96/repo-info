## `julia:windowsservercore`

```console
$ docker pull julia@sha256:91949f9dc6a2ba335f38712cd941eb739d1c64a260fde1059319857eab40e0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:ac7e7de1919e6a391278fd06062034d24dd1892f6569260439ea7a8aac745dd0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2161166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f26f77914b415046af8c139841e565707106b2048fc516c6c1cb8347d2a4f8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Thu, 15 Feb 2024 01:55:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 01:55:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 01:55:59 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 01:57:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 01:57:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ecd8f02f1b59d6f3aec1c570f2c8128d2b064a59e0da86653fdee442a472ad`  
		Last Modified: Thu, 15 Feb 2024 01:57:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62852f81701e842eaa34fb5baf41629e3a8bd717a09aeae6c9d8f85aa6d3d870`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1387c2ad061bd6ecc5941ab04b037b84018b2bfddaa265150d148ffca73b4`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3360ff5dce5375b4b898a4f4deb9f588e12659cb8db5611d7e3e01952b012`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ebaee761d2302e12dcc0f6dc0d9e5debeb07658857a8749c1f96a07fa3bfb`  
		Last Modified: Thu, 15 Feb 2024 01:58:16 GMT  
		Size: 250.5 MB (250505768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c23a6fdc0fc3d51f4f3676cdf3a438f7d52cb9f9a6a964c4645f304cf900ff`  
		Last Modified: Thu, 15 Feb 2024 01:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:0955c5756b87875173c9a5b65b2df8cbb7d5b390c9c4550f7f521c40b3fa1935
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330962381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0a0692cd89c0ebd705bcc2f6c2ddf0fa8c2f800111fbf1041ec324ce62832a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Thu, 15 Feb 2024 02:05:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 15 Feb 2024 02:05:41 GMT
ENV JULIA_VERSION=1.10.1
# Thu, 15 Feb 2024 02:05:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.1-win64.exe
# Thu, 15 Feb 2024 02:05:43 GMT
ENV JULIA_SHA256=ca02e6bd4f771d51c72520f359d727679775c03f62e7e7e2595dd79d1d0e5fec
# Thu, 15 Feb 2024 02:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 15 Feb 2024 02:07:21 GMT
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
	-	`sha256:54ed3e36144d60ff8117a3dd6eb64daa4e29953bb129aaad397b30092f9cc4c1`  
		Last Modified: Thu, 15 Feb 2024 02:07:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff9d169a5e63801023c2b6a0a537977e5c7505d96e3c8896d7dfeadf1d0072`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948476976b5affd175205c3463e19547505c660c8d62ec0c51a0ccab24e7a100`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066dd587e2e5fd44cc77bcf785a1eda6cb2c8fbfea705e112683712dc9bbf45`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de535d017baa9a7dbbcba70d7fde8cdb8607907fd1752fa99946ddf57958b2b0`  
		Last Modified: Thu, 15 Feb 2024 02:08:00 GMT  
		Size: 250.5 MB (250507125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858c84143178e070fff903c762901603d1b1356e962f4fb73a71a200a55c84c`  
		Last Modified: Thu, 15 Feb 2024 02:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
