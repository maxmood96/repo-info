## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:f4c5447aa92c62ef7652b96da7658371c2117b42658326460c62bd8314c8fa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull julia@sha256:8a2e0461f9da6fd8e90629ebb384664c224a4c27399887b0514eadfe9314c109
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3719053576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6d7dc54b03b32f4327b222d8d71719538bf836e3f012387407fb6be6302318`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:53:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:53:58 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Wed, 14 May 2025 20:53:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta3-win64.exe
# Wed, 14 May 2025 20:53:59 GMT
ENV JULIA_SHA256=1aab913a2acd82a1eebaa63e958d3d5741306aad93ac663afcee5791691fe96b
# Wed, 14 May 2025 20:55:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 20:55:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f832910e4a3299e73e50895deca18fbec2cc00edca6702841d48e77bcfcba1ee`  
		Last Modified: Wed, 14 May 2025 20:55:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66ceb1e4c118cc44b9383d28381c8a8c10c1e506aed2bf65f45a2d79eecb9ec`  
		Last Modified: Wed, 14 May 2025 20:55:12 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8251c63495338f28fecad4b5b81e0a3b3311475a7e3381ebaba4a60e52613a23`  
		Last Modified: Wed, 14 May 2025 20:55:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9c4e918d9421966a0ff33c8d68c56b1034b0572b93a4557a80d25bb97b77d8`  
		Last Modified: Wed, 14 May 2025 20:55:12 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b621a996edcf4b05a6bfabb8575b724e3ebeb14eebb0bcc8a93cbdc242c8652`  
		Last Modified: Wed, 14 May 2025 20:55:57 GMT  
		Size: 288.3 MB (288281176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9ac8dd5b45619f4a539c4195d1e4a0cd4b7ccb8f13429c7655da785fbc01d8`  
		Last Modified: Wed, 14 May 2025 20:55:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
