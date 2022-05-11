## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:179f37b944f60d844398c6d45b8f00fa183a14bb4a45716e992c0aa29a9a79a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull julia@sha256:2e507ea4b4f2dab2f5d77225e75dde0ebb7fa20e4e7db9a85e88574cb6efcb50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2382551345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d80e8829c64c53f597560f374903a270f6ad80c3a4acb10814b2cf729cd9b7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 14:16:07 GMT
ENV JULIA_VERSION=1.7.2
# Wed, 11 May 2022 14:16:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.2-win64.exe
# Wed, 11 May 2022 14:16:09 GMT
ENV JULIA_SHA256=bede21e00130c2dcb6973a968b7ed43c35d69712008a95bb08d5536d3c9e2585
# Wed, 11 May 2022 14:17:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 May 2022 14:17:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221495150b2d715eb091575863ccd8f7cf4165a24ac7dfccb48213a94c32447a`  
		Last Modified: Wed, 11 May 2022 14:30:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b50f50acdd862937b30e58eeb185113d6540d8c41788446bea3d29a27cfeda`  
		Last Modified: Wed, 11 May 2022 14:30:09 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438d15db72235df8b429f3d8386c96e009577b464b2d7f97ebabf9c76aaaf86e`  
		Last Modified: Wed, 11 May 2022 14:30:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef41e1248ab1ef37861bf446f2047f576f924b5742eb3eaabc45493650aeff78`  
		Last Modified: Wed, 11 May 2022 14:30:43 GMT  
		Size: 145.0 MB (145008974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2fe6d9cd29cd6ea050436bba40b46dcb60cf30b51ba3c9558a79d5675d053d`  
		Last Modified: Wed, 11 May 2022 14:30:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
