## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:d847524a88befd782505a0e286ebee1690e4ae6e7350fa7e0e08b6ff95c256d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.7462; amd64

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

### `julia:1-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull julia@sha256:155586ca85c265a2c7511cc1655844cf42357633c2117c372548ad4d1051e732
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167041442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ed765706c67cfd16604443d4a4c68ef162eeaa9defd2ca4940a9047939ec7f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 01:00:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 01:00:54 GMT
ENV JULIA_VERSION=1.12.3
# Wed, 17 Dec 2025 01:00:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.3-win64.exe
# Wed, 17 Dec 2025 01:00:55 GMT
ENV JULIA_SHA256=ab6f046e7302195c253280534f8233b4597ae2f2758d3699d32a7c161ed12690
# Wed, 17 Dec 2025 01:03:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 17 Dec 2025 01:03:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbc6fee2bb8df090e22909d61c1bf04c0a714bd10f1d2b941676e504a0a1fed`  
		Last Modified: Wed, 17 Dec 2025 01:08:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0fc87b66ef4f76b47401e67ef9bb67b1743b2f2f6dd655386ace84f36a1fa`  
		Last Modified: Wed, 17 Dec 2025 01:08:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcdf1b8cc94519f576299eac34ea4c6db7e8d28a8c47bb0c6c909077933886e`  
		Last Modified: Wed, 17 Dec 2025 01:08:55 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78c5a7a596636a511eebc06a0069e0733b743517df7c1138cd9657a2d67ad0e`  
		Last Modified: Wed, 17 Dec 2025 01:08:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c980b25c013f44f5de770df7e858cd3d318edf3c60b5238e7ae26187309917`  
		Last Modified: Wed, 17 Dec 2025 01:09:05 GMT  
		Size: 387.2 MB (387155565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c07db36652d94694df2033a4a8dbdeca2b2ebaae5c47e0e80db063d43bf2162`  
		Last Modified: Wed, 17 Dec 2025 01:08:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
