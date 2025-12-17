## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0d4bc427ccdcef06808c2b63bbd8878b1e282cbae55c15d0f6629eed3815dc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

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
