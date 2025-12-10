## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:949eb817ab986d43d9b58c3e5aba57ffb59b5182b1ba58e858d20a5b0d2b7a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull julia@sha256:5a6338c253e019e0204d9e2d9d98e89b801cb075a5dbb126b1510d83f15aaa56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2165978101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480c27f3a3c9cc5e0f01c408773a3f602c0350fea897997ae0aa8e54cb243895`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:32:46 GMT
ENV JULIA_VERSION=1.12.2
# Tue, 09 Dec 2025 20:32:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Tue, 09 Dec 2025 20:32:47 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Tue, 09 Dec 2025 20:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:35:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4337b0b452250939272a24a7d25392c5f6351fbf9da067a0d397cefbb4266c7a`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c6c5577de4e171f25b235ca6f8a0adebf834fe9f056f30433b8639145f99ba`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa80e94aa03accb23f8d444de9fe4c73941bbf916c68dcfe845cd2118f81856`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f0c9df9c3e0662ae962acfeec828cd6bb17996ee6a8444f2d4c25505b1ddaf`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2147e4adbcc9e9f51209be098aa739258b406e821fa9d85698a386109e14c1f1`  
		Last Modified: Tue, 09 Dec 2025 20:40:57 GMT  
		Size: 386.1 MB (386092289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21433acfd914605fe1899281b94af10aa9480656be49a66b9d81c4de427085f8`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
