## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:6bff7a48a08d96d7d7dc610f24a2b81b4b5d0efbd87d6afa16befcdebe764b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:fc9f5fa18a9e452e88ab7e13cbf1b84f20db7ac193243fbab049d55af19e19ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3518049644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870fecf81a58bab81b1d10c5374832dc57f826f86ef3a491c1ae208934219c8c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:23 GMT
ENV JULIA_VERSION=1.12.0
# Tue, 14 Oct 2025 20:43:24 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Tue, 14 Oct 2025 20:43:24 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Tue, 14 Oct 2025 20:44:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39784c98a529060757c92dd68295796743ba6078bab924b6aa3db930523bf7`  
		Last Modified: Tue, 14 Oct 2025 20:59:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c18da90f047c377c219422c6907593904b75530cbb4d0d8612ed807acc16d`  
		Last Modified: Tue, 14 Oct 2025 21:17:23 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e783b61199dd61b2ed477c0241fb7ab85dc61f54c8f133b01160a892be2cbc`  
		Last Modified: Tue, 14 Oct 2025 21:17:28 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b7a205445adc258bdb62d929a8db2691d180a289541939100b43da825136a0`  
		Last Modified: Tue, 14 Oct 2025 21:17:32 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb3af1ef53b2d92acdc6df1e569a5cb109c9380f17aaaddaa552544fccdca51`  
		Last Modified: Tue, 14 Oct 2025 23:02:38 GMT  
		Size: 297.6 MB (297562559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba6984c0909af3902b4791248dd6040171be4aacc9ae95c0578988d6b4d58b3`  
		Last Modified: Tue, 14 Oct 2025 21:17:35 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
