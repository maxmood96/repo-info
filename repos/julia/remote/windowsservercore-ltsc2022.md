## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4426e2a8c83587fbc2b48d4eb2521fd9d412bc9cb7f6465a5c221e1712b6f1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:b7e156aba083610d402c4deb76f4d0cfeb007cfa19fe247ed1508da984f235cb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2534985039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd056668a793e45ef8c7b40abfdf7a4dec7fc8672ce5e0ef6b2076937a27e49`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:25:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:25:58 GMT
ENV JULIA_VERSION=1.11.4
# Wed, 12 Mar 2025 19:25:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Wed, 12 Mar 2025 19:25:59 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Wed, 12 Mar 2025 19:27:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:27:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd17a49f6a739835ecc0588a2ee05921152a21b6254b17fe89eefc650672244d`  
		Last Modified: Wed, 12 Mar 2025 19:27:24 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216df18b94860cde089178216a598fd88c9828c39340823a0d47e15014cd8cd`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41306a625e141f7336a5eb1de893351034f4f0765f4f6fd84353eab11d45578c`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f404eb1cccb63d04050cd1ca0711a31fea176087ebcf0fd868d1373664704532`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadbacf47be8fb49f510a4d80bb9de78f38df0507aedaaa32f9614ce6e38a1dd`  
		Last Modified: Wed, 12 Mar 2025 19:27:58 GMT  
		Size: 265.0 MB (265037405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c647a37a1afbf0781145203ed926c5bd369d074b8a165bbb369bbbe096587db`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
