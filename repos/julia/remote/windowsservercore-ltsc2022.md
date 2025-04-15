## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2a95a0cfe2d6a997cf744322c77dc9ebae9a9016f61d7c76b5e2db91d4f1c16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull julia@sha256:4692a238c3a42cf0ad01ac03858884d3c39d65933efc0e3bf99bdf310a5d557b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556462029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da15b5affb2d343f2e5d168430aaaeb121e4339abb5a0283440d268849fa419d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:11:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:11:27 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 22:11:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 22:11:28 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:12:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:12:49 GMT
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
	-	`sha256:0668eb4ab6538a007d7d921f86dc81fc9e022fd4281369049af6b80a4ca828a5`  
		Last Modified: Tue, 15 Apr 2025 22:12:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945d11cd5e04d63d6222d3278f37c4dd6d6994df62da17aac8e71ac22f1db208`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201bd3be521ed32686d3e4564f52d6bd04aa55f25883d5479fc22c38aba4d32f`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5decd5cb85982b35960661bf50aa7eeef035d39f2799fad05c045df687a67a`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ff4897cace2368d20d6984fed7f68f1a17c1fac2bc1231d8fe911a0f7f62b`  
		Last Modified: Tue, 15 Apr 2025 22:13:29 GMT  
		Size: 285.5 MB (285459956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c626e16efd1d216f79e2bd6ef4ee6c53c79fd08210696141dcfa6c7dd8a1ef0`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
