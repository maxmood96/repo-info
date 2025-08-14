## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d1333599d1a04e8d7043e46de18667b137409a2fde761ff0eb56247cb2656c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull julia@sha256:625447d3dde2bd9c7972879d208c9a0f1304e474077c34ccb074cf3c263abc31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567555274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7473c348a9a50005201b43a4097f500923821d90cd8da9dd6ffa74ad9b9cf5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:31:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:31:53 GMT
ENV JULIA_VERSION=1.11.6
# Tue, 12 Aug 2025 20:31:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Tue, 12 Aug 2025 20:31:55 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Tue, 12 Aug 2025 20:33:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:33:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8663c4d2d36718aae1a419811e3600ed879d9244dc2e62a0de02522fc61245`  
		Last Modified: Tue, 12 Aug 2025 20:35:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcaca73cdc24156b5bf4135eb5726487883d8e47fb96541f9e68c05d0df559b`  
		Last Modified: Tue, 12 Aug 2025 20:35:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca570c3f6615c5bd81b96869e558a33852ed19e96d5b9d70a12b218b739cbc6`  
		Last Modified: Tue, 12 Aug 2025 20:35:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71971d011d5acccae7591a17d16a43c9c9e1c1b75eacf47b43ddb4ba0c8d8a58`  
		Last Modified: Tue, 12 Aug 2025 20:35:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368098632db31528abe917b1e3b08f8d7e01930b928be89059c13df00977b956`  
		Last Modified: Tue, 12 Aug 2025 23:04:43 GMT  
		Size: 285.9 MB (285856859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9f044d4f7b2ed5beebbd8ef7693d2c740455ab29f250364880b8808e57cfc5`  
		Last Modified: Tue, 12 Aug 2025 20:35:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
