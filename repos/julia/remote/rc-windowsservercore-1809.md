## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:a61254e971172e5e60101c2626919f8f98af9407a98511b52a16a3407a6cc82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull julia@sha256:7384c7a03c2f211cb945d800bc36cad4a9bfe3ee53780596ca32c039ccc580d0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2233528009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3fc5523a6d304fa7ae57dde6bcd89e45d666cbfe7f3176c78a67a1838ae9d1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 05:26:25 GMT
ENV JULIA_VERSION=1.9.0-rc3
# Wed, 10 May 2023 05:26:26 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-rc3-win64.exe
# Wed, 10 May 2023 05:26:27 GMT
ENV JULIA_SHA256=5cfee20b00591abb548ca32f4931e52284e831c783238cba72e6f9622bf5e76e
# Wed, 10 May 2023 05:28:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 May 2023 05:28:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f362f6f756957bb99930b184b25d3aad07a7f5057272e3008e4c18b2ae6fbdf`  
		Last Modified: Wed, 10 May 2023 05:36:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627186f2fd2157af57b1b2348aad0cb2f9e19ca7825cc1917921f8c2d6b44d53`  
		Last Modified: Wed, 10 May 2023 05:36:55 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb6fa3c56fc6c220c2146ec98e4ee4e8bab5505cceae5b80c1b0f8f371b2313`  
		Last Modified: Wed, 10 May 2023 05:36:55 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5e58269f27cbed620ed71bb52bccd3c7a35d9201ed1fafc9806837c8d9b749`  
		Last Modified: Wed, 10 May 2023 05:37:27 GMT  
		Size: 161.5 MB (161485685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b828064f6e666782e8cac21cba91f6baab1e9470766d752d4ff75f0bfe5a80c7`  
		Last Modified: Wed, 10 May 2023 05:36:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
