## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5282326dbdc5f74ab85db84eb5175f4eb2793a1a7e64310e2c9eb51970032efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull julia@sha256:b4ad73e9244864d5cdd16ac66875c1b092404d061452b17eb30817959a36a26b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2559103838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e38f4f60e5482851ca8eb48ceace98c4fb3e91ea2540adf2723c774f1261452`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:53:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:53:12 GMT
ENV JULIA_VERSION=1.11.5
# Wed, 14 May 2025 20:53:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Wed, 14 May 2025 20:53:15 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Wed, 14 May 2025 20:54:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 20:54:28 GMT
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
	-	`sha256:fde71cf7f0206f9066b360727ada246c35e8c2213ff03371123ce5f0b60d846a`  
		Last Modified: Wed, 14 May 2025 20:54:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a097034316c1b8634696e5b29113a4f9ad42f91af3af36ec21900b32f5b4736d`  
		Last Modified: Wed, 14 May 2025 20:54:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c3a9b1683d807b6098e51cc30bc497423fb0cd532bd57db7ad40a8c8ff4e0c`  
		Last Modified: Wed, 14 May 2025 20:54:33 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00aa06ed94af7b4e2bbd843cedcc570e7826fa9890aabffbbd453f84c30b13dc`  
		Last Modified: Wed, 14 May 2025 20:54:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4219da80fe59508d0d09f03af1f00bf4f7b21a83dbfdaebfc6e838b7b829eb9`  
		Last Modified: Wed, 14 May 2025 20:55:09 GMT  
		Size: 285.5 MB (285469306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2db2d9feac456c86c472a5cc214ab75fc468a10ba17a7f4d0a7016b9ead932`  
		Last Modified: Wed, 14 May 2025 20:54:33 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
