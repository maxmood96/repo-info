## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:12f1c302e427ca303064f40c8b0d98ee4451929991b6da9253cb358123f04831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull julia@sha256:70254e22e0c007fbabb591d88a4321d339757c6560f4cf0d15c599eed88f74df
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561825036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce6786742510eb5d3fde0beaa402f8b0fb1b765a4dde95c08d7b148ddbee3ad`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:27 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Wed, 14 May 2025 20:58:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta3-win64.exe
# Wed, 14 May 2025 20:58:29 GMT
ENV JULIA_SHA256=1aab913a2acd82a1eebaa63e958d3d5741306aad93ac663afcee5791691fe96b
# Wed, 14 May 2025 20:59:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 20:59:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9678c4b6843d52cae426a1c7302fd03d242df00eeca6b4f0530390f8a574c446`  
		Last Modified: Wed, 14 May 2025 20:59:53 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481f33820be9eca9910d6f2c2f1bc5dd8072c3fb55bf485638ebda00c6bb687f`  
		Last Modified: Wed, 14 May 2025 20:59:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a33ef11cdcaab7f545ea1ef4e1f0397d9a75c3dccd5c919e1d4621c92a6917`  
		Last Modified: Wed, 14 May 2025 20:59:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec67568f483bc04e949697f0d4a011e3d6c889144df0bd8f579a20d180481519`  
		Last Modified: Wed, 14 May 2025 20:59:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8552dc6fea7fb05b109eab921c7dc94cae6da3b5a7b4aeae1b8629123232470c`  
		Last Modified: Wed, 14 May 2025 21:00:30 GMT  
		Size: 288.2 MB (288190492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0159bb4d1e7d158300b799a6bae39b3e614ca70c21925ffa1077b4711ba8d766`  
		Last Modified: Wed, 14 May 2025 20:59:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
