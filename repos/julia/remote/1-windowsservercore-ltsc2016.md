## `julia:1-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:c8305da3fa05a576b9026f4933ff13d4b3f0c1477caeb265faf2e00ff817be5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `julia:1-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull julia@sha256:569ffbf1840046fde5a4c6857a546ee8657d1295c81d26824ac4d284f949e6cc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6405360495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4115203aa48afcf380123b3d27df35b51ac08e1362c7eb35c4a83d613dbe4d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Sep 2021 02:18:54 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 28 Sep 2021 02:18:55 GMT
ENV JULIA_SHA256=bc43b8729dd2d95d9d148ada989c8582a66e99af89fcc91d8ed41ee2f13a9985
# Tue, 28 Sep 2021 02:21:11 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 28 Sep 2021 02:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa8ce1bc1bf7a234de8884c141a77aa6daea8952a85cee59ef7f8050ad5d020`  
		Last Modified: Tue, 28 Sep 2021 02:25:51 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef3dbf26f73aef613b3635bc356453c4affe9ef3453a0a762e61f16b17d86f7`  
		Last Modified: Tue, 28 Sep 2021 02:25:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b33aa58de47268bbf58faba1fcb08676bcb8d5715d1a7d599cc7271d947609`  
		Last Modified: Tue, 28 Sep 2021 02:26:21 GMT  
		Size: 134.0 MB (134027074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d73c89f104657e4222d23279b44db569da068538c877fbe2b501aaec79414d`  
		Last Modified: Tue, 28 Sep 2021 02:25:51 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
