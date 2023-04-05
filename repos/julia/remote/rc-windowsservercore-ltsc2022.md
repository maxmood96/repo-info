## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:33360a1a79fc7e6eb558b75bf9b1d640f964d8e8d0bac9f881c9ec526e78285b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull julia@sha256:30cced8799b30e70f7f09a524bc6b258cde12fd69a5404f9a293f773d584078b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875703958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0fcd9daf898a37489ab4646c45af6512e25805c31aa950a9730da9206d3f3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 05 Apr 2023 17:15:18 GMT
ENV JULIA_VERSION=1.9.0-rc2
# Wed, 05 Apr 2023 17:15:20 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-rc2-win64.exe
# Wed, 05 Apr 2023 17:15:21 GMT
ENV JULIA_SHA256=ea884f779347b1e307b62b1458ed0430de23259b69016004ef5271736d77309c
# Wed, 05 Apr 2023 17:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 05 Apr 2023 17:17:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff1ed8d7f177221d52725b5829bb6e60493f43f24badefa9590a85e2d749878`  
		Last Modified: Wed, 05 Apr 2023 17:21:21 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25196546f030ddc1ccf55303b05cdfcb8d50b240c3e0a141be2102c3b0d7f73e`  
		Last Modified: Wed, 05 Apr 2023 17:21:21 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aea1de92cec33dd2b50c8ee3dacaf84f957a7ace3ba0fd0b17d49cff0a3a58`  
		Last Modified: Wed, 05 Apr 2023 17:21:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4a5657682ae11a6db263f5d4c6c5e3483c26af2181304e2c6158c1a89b55ee`  
		Last Modified: Wed, 05 Apr 2023 17:21:56 GMT  
		Size: 161.8 MB (161756818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a9aef4b9b2866208f1086b930634786c5760effc70a535a3893c481bc7885f`  
		Last Modified: Wed, 05 Apr 2023 17:21:21 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
