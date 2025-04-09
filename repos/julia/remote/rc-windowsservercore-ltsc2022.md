## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cbaa9e0b454c5835cb93446fd7ba1bb5b4656ffca5b930671b2f18d275f7dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull julia@sha256:c468ed3709032e3c90cf21f770ef5f8c762b32e42b8ed509bda941f85b2ee5d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565459500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6358d7a152a5ba9167451f45cb244e7f6ffcbeffb1dbf102bfa7a5cbdf966d3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 01:53:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:53:07 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Wed, 09 Apr 2025 01:53:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Wed, 09 Apr 2025 01:53:09 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Wed, 09 Apr 2025 01:54:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:54:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a269ff92d9ee8a3145e4f0fb4f9a8547e14e1c441621f71d5e294006db51fabc`  
		Last Modified: Wed, 09 Apr 2025 01:54:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29900243d33ff01b9e0bdfb74460c556a41af35212d7aeb3b599158c59f53aa`  
		Last Modified: Wed, 09 Apr 2025 01:54:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e9dd3d5f8c49434f38a72bf06aefa6fcc28d96e26595441ad43be25e00657a`  
		Last Modified: Wed, 09 Apr 2025 01:54:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecce5465352d2bb8698c4414849492981651ae3f4f5df6a799cf40546bafd36`  
		Last Modified: Wed, 09 Apr 2025 01:54:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc0e102fb41640683cfd26547b3169b6df85f3bfa517b5cc0b372b8d4c3fc1f`  
		Last Modified: Wed, 09 Apr 2025 01:55:16 GMT  
		Size: 294.5 MB (294457379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ba3c9e84bb4b0fa7a05fcdc2f2fce7efbd422543ad52584fb98d485e71b4`  
		Last Modified: Wed, 09 Apr 2025 01:54:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
