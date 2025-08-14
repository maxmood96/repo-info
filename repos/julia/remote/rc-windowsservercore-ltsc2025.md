## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:9b9185f0dadd22f37a5190c7007aa2318b36773d249571b07eaf2eb415d77f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull julia@sha256:beec6737f55330653912657885996d0f403e1946e007efa02c1638dc518b5fce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3781725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e90250295b378178eb03eeebf68b2b655b9f5c5370650abc5e32cde931ded7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:49 GMT
ENV JULIA_VERSION=1.12.0-rc1
# Tue, 12 Aug 2025 20:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc1-win64.exe
# Tue, 12 Aug 2025 20:26:50 GMT
ENV JULIA_SHA256=34569cb903c4713787ee8f1b7ddb1a8c57e44f64b1312eb80635ca7041aab409
# Tue, 12 Aug 2025 20:27:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a793cd72533800ca63d169208ab213901b66f4b95b6904d37056c5ebb9b0242`  
		Last Modified: Tue, 12 Aug 2025 20:31:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e60664b32b626a022c344bbac1cfe401205ed082ff960da47747bad2503160a`  
		Last Modified: Tue, 12 Aug 2025 20:31:39 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9c0c648fffdd7fd49c67aa4730e375c3800c670e77e011b18ff1864d69ab22`  
		Last Modified: Tue, 12 Aug 2025 20:31:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296cb39287e7c326222e7a54de38367fdc696daa33e664232c0504342b845e88`  
		Last Modified: Tue, 12 Aug 2025 20:31:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cae346042aa726b67034d95fbdee4175ce8644cdfe2043bede3d8a40242df5`  
		Last Modified: Tue, 12 Aug 2025 23:05:38 GMT  
		Size: 282.9 MB (282889012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fb5c4ce0b6ce1d71aa1ea80474e52a5c47d684adb8c07c59b0f3cc290e0fd4`  
		Last Modified: Tue, 12 Aug 2025 20:31:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
