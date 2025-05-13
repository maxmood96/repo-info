## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:7d0fd99efa6176ee8911bf90b9a736fc6e6f9bc31ddb2571428c768bc74e824a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull julia@sha256:1fba878326f2252995b21f035fc59c0e659f8837c9bc998efd68dfc4e2506483
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2561804690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81431807cf4c31e534d25d494ee113b43e2e5ffdf98ba183478466a46b8a3674`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Tue, 13 May 2025 19:57:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 May 2025 19:57:38 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Tue, 13 May 2025 19:57:39 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta3-win64.exe
# Tue, 13 May 2025 19:57:40 GMT
ENV JULIA_SHA256=1aab913a2acd82a1eebaa63e958d3d5741306aad93ac663afcee5791691fe96b
# Tue, 13 May 2025 20:00:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 May 2025 20:00:18 GMT
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
	-	`sha256:f23864d7936037432368e4b05e037bc5edb972e038de774579643f803a72144d`  
		Last Modified: Tue, 13 May 2025 20:00:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc0c20851f8528aac001980b7feb300537280d7b885c4c575d9ef2f554a1c4`  
		Last Modified: Tue, 13 May 2025 20:00:22 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd516089a1364837b560286dec68f0b032f46b2a51ee8bb2fce4fb1f34cafeb`  
		Last Modified: Tue, 13 May 2025 20:00:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef682c8a69fd569d6a8112d257c72a84bfbaebebf77be05f980e63726f87639`  
		Last Modified: Tue, 13 May 2025 20:00:22 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc5a0b7c4f03fce806a8605f2bb5fe7819d3649fa917b036e5cdd1e4e109d2`  
		Last Modified: Tue, 13 May 2025 20:00:59 GMT  
		Size: 288.2 MB (288215704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c95f5561d7a73c2f8002000389769b675b7105fa778bbce7a24f4871f0c1a`  
		Last Modified: Tue, 13 May 2025 20:00:22 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
