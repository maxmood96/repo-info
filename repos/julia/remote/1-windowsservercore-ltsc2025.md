## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:8f5238fb422a2cb2927bfc48cb27c6c02f3eb39f5473e121c291488133896f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull julia@sha256:309f0bb4c7659eb614dc41ceb0747ac18dab07c0e0e74cc2e96540e9e6650dac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640171749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba84fa4ddf9821952b035fbbd715f28c5ae869b4ce9f2a0e638aa8d57cd10b7b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Wed, 17 Dec 2025 00:20:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 00:20:31 GMT
ENV JULIA_VERSION=1.12.3
# Wed, 17 Dec 2025 00:20:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.3-win64.exe
# Wed, 17 Dec 2025 00:20:33 GMT
ENV JULIA_SHA256=ab6f046e7302195c253280534f8233b4597ae2f2758d3699d32a7c161ed12690
# Wed, 17 Dec 2025 00:22:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 17 Dec 2025 00:22:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c17bdd0f1de245543bcf5912e47fac7ba41e04a89b62ef87e8422a32b81bd`  
		Last Modified: Wed, 17 Dec 2025 00:31:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c0215734968ce2ceef97666853ad6a59ab33415c5167d7a0dd3003f6feab9`  
		Last Modified: Wed, 17 Dec 2025 00:31:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3697f7de37ebc429a4dc002f3f0db27315c84e1f1309b34b1a823dc08da07c89`  
		Last Modified: Wed, 17 Dec 2025 00:31:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc84c021334eabc2cd42c6705c1d1cf652678d15b6487826b5eb792522c325a`  
		Last Modified: Wed, 17 Dec 2025 00:31:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f728eddca48c039edccc2e10a742fc87ea6737ab10058d17103c599bb991670`  
		Last Modified: Wed, 17 Dec 2025 00:31:46 GMT  
		Size: 387.0 MB (387044780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b06e485703063cfa28150daa8f8b4eb5b7680e0ffda8e5b6dcb9d163fc1d`  
		Last Modified: Wed, 17 Dec 2025 00:31:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
