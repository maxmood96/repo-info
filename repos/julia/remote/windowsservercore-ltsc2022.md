## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:3e81e5b0b92dc2c2d1ba31847ca0964d4dd9905ef37e07e4b655ef8098c0d842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull julia@sha256:17f43aeb71a79fd1b12d1cfe98b42214174edf236e1abad28ae90a10915a62d7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2566470006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bc60a8d798c73732b1c194bc63064e4eda53a32794c5c6ff98d5871258e89f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:40:32 GMT
ENV JULIA_VERSION=1.11.6
# Fri, 11 Jul 2025 23:40:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Fri, 11 Jul 2025 23:40:35 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Fri, 11 Jul 2025 23:42:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 11 Jul 2025 23:42:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7cfbce764c045a5a8be78e9a535ae558a4d5b79c31255fb8cade2613654986`  
		Last Modified: Fri, 11 Jul 2025 23:43:31 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4133596cfbb33bbfdd792d82f93df6e38e3d263f16a6b4ca48f4e790f68dff76`  
		Last Modified: Fri, 11 Jul 2025 23:43:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1159137a29db227d18bb9a52adc250d1008f723ea08cb57b543829436f445666`  
		Last Modified: Fri, 11 Jul 2025 23:43:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a308b3012b610e569100be384f0fe7e9ffc82b9a46ba38a90a912be7af1ebab`  
		Last Modified: Fri, 11 Jul 2025 23:43:31 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f864da7c61f910a6bed3ddc1feb8c8e6c89346b657643f612da46f988b40bbf`  
		Last Modified: Sat, 12 Jul 2025 02:04:05 GMT  
		Size: 285.9 MB (285860083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2ccc19ff9e131d1b4270cdc9e6eb4eaf6ce027d68aaf67bdccf1e7754340b`  
		Last Modified: Fri, 11 Jul 2025 23:43:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
