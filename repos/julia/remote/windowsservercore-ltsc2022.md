## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:08d4783211ed9a588aadfe7e3f5c6ec3d1ea6e62c78829fefa5400c8ba3ad704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:182b17c903a2a430ca241abf41714877477e4a48098d97015efd5dacc9146a29
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156064808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a0a6fa09d0c43d7168f5e629beb272ed9aa78e88a1a938239bf46c19de25d2`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Sat, 06 Dec 2025 00:35:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 01:06:24 GMT
ENV JULIA_VERSION=1.12.2
# Sat, 06 Dec 2025 01:06:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Sat, 06 Dec 2025 01:06:25 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Sat, 06 Dec 2025 01:09:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 01:09:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8462076761531ece541cabbff8aa81904d45ff8a160c631ad6c756c28992e1c1`  
		Last Modified: Sat, 06 Dec 2025 00:45:14 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ccf31c85b482c150ed97cfc6f6b268ddf0091d66cb56eb993d8641f2cefb61`  
		Last Modified: Sat, 06 Dec 2025 01:10:49 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f1f181f88ec0f43cdacbea9ab02299e6c80e2369605e91137b1f1b51982a4`  
		Last Modified: Sat, 06 Dec 2025 01:10:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89e783b8f4296a56d315dfe1eb7b5d26a9e81f2a928f5f335893ce6078bd078`  
		Last Modified: Sat, 06 Dec 2025 01:10:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c6ebd1f1169d4079f949a72507f16c941c87eee6bfc01831ec3f1cd6d6c301`  
		Last Modified: Sat, 06 Dec 2025 01:12:43 GMT  
		Size: 386.1 MB (386096781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd62c859283ed30563bad9938bcf852fcc50b5f4f140b75eb217f60bcd4719d`  
		Last Modified: Sat, 06 Dec 2025 01:10:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
