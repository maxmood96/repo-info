## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:f28bf0aea9005f3adf7e41564c52e22892bcd73aa5880e8e142220fca3959a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `julia:rc-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull julia@sha256:38a4688834b09230471668f625747043c8115544444886e9c8481701526a8388
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3689718330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b990ca274f7f09fbc591e36d3aaaf2a0570e13f65827b84eee4970276f46eb5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:13:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:13:39 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 18 Apr 2025 03:13:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 18 Apr 2025 03:13:41 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 18 Apr 2025 03:14:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:14:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d847cb8729cc156a33f45c8c7fd3dba8d388fe1250452da78b91c429cac4143`  
		Last Modified: Fri, 18 Apr 2025 03:14:59 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293df24207b4274e8ed7b37864525eb87c3c117a30061355bd7ecd0208ea130`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6819b0563ab53578e347dbb7d0fedfa705d74b359dcfc728656bbc991e85a`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c4090a6becae243511e5f4ccbc3b40b8d8fce71d490360bc9a11d92ce9614c`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cda6730a3455bfd35603b180c1776210a5e2a9829133041ccb893f124c52692`  
		Last Modified: Fri, 18 Apr 2025 03:15:44 GMT  
		Size: 294.6 MB (294550449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df01aa3bad151b8392149d9e97bd5dec8dd71f6835fe3cee04564fdf2e6c93e8`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull julia@sha256:61e62bac5695e0ab3a86ab2cd9244acbfe12bcb374b2fac5478e42dbeb18b706
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568050577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7315bd3eda65b33c5ba73df3a449b6ef70d7f6243312dbe162d3f6297d3d86fd`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:19:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:19:47 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 18 Apr 2025 03:19:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 18 Apr 2025 03:19:49 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 18 Apr 2025 03:21:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:21:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3568cbdbc43f2fb73f80e4cb09a4c8cb71d414c5c82ea37bbf228fa2d87f8`  
		Last Modified: Fri, 18 Apr 2025 03:21:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9494a98b0128ae2301ef8402b5dc2148714b22aa597c4345d06c2a1307d7d32a`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f94dbfdcc063cbe794e4b806184800c859fdd83f969a41229f55c06feea40d`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27b45c50068f924f3a10356825ed81b314cdc2e661ae9641c867a9df94392f`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a67ec52f702b09267c549dc67f22904376deea6317b6859e8cca05499f805d`  
		Last Modified: Fri, 18 Apr 2025 03:21:51 GMT  
		Size: 294.5 MB (294461605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d909081ab78526e7e396945acf2d46386f93195387579982855168a452f8e9`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull julia@sha256:a9b0afd064ca2650750f9bde62acf4c60f291950c529e6c461277054cc172525
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459989078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90a7e3eac73cc314638b907db197ef43213cf8e86690c031540cfeb0072fda8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:14:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:55 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 18 Apr 2025 03:14:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 18 Apr 2025 03:14:56 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 18 Apr 2025 03:16:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:16:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea57d6e0a3fd854ce9629fe9fe87f545ffffa36f52dd5c56e985a47f44289670`  
		Last Modified: Fri, 18 Apr 2025 03:16:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b463d1e95170ef10a02abcd943e06f1b315fb61ddbdcccc3d0f4573fa2d788`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a35d996f03bfacd5085156de4e2220699d1a19d028f422dfc8be8652507c1a`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd361573e02e63c3a3c8445207e810b88509fd90e272b488b3fac80304b5b1f`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8015c1070d96733e69318a94355a7640dad8526a40678f924508af2bf023a2af`  
		Last Modified: Fri, 18 Apr 2025 03:17:19 GMT  
		Size: 294.5 MB (294456803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76294b70e11395a457780fca63b1b41dc5485a2ece93cae13a98b8ab22d30be`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
