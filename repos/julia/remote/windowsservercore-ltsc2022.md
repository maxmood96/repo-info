## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:fa010417fc5396873a3773e566943ac323ec900e41f6cea1fa47bae7435d12b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull julia@sha256:35ff2d82eda048ca16d0d8eb20905a52db8f3531e5f5ede13186a2fb394cbdee
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5150180c61675eb08de51ad2ba1417ad6f4fd04da20972fd886fcff56226d07`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 23:55:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 23:55:46 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 23:55:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 28 Aug 2024 23:55:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 28 Aug 2024 23:57:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 28 Aug 2024 23:57:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e86a373484a9226fb2951ac111cf61075374106381e25908fc926acbc6a056`  
		Last Modified: Wed, 28 Aug 2024 23:57:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25995c4cf169543f430445558d4c95aa6434766142bbb601ec43d1c537496a4`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66b8803d7228f9507e69ed2aba00848562367a5db6a1162e7a9f9a97dc4928f`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f7fc5b58fddfd1a3f9bcff4c4b6ad062847af85867a169074e877efd03e17f`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3412e707947fdf51a0772fd74c974e29ea85b079793fc9416f6b133f51585bd`  
		Last Modified: Wed, 28 Aug 2024 23:58:11 GMT  
		Size: 188.6 MB (188598911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85bd03d8438c88c9b546fbd749dcf5d9819ca8dec46c49e7408bb692db3e485`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
