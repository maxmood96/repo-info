## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:4ed783d3f29a5896b365fb6cb8e4d6b799ada5a44c87e720dd6f064484bf0442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull julia@sha256:fb48637bbfd49062eee76992f0500f6936be2d7e6f5c5809e4b92a87c2cf584f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2819481897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad2513d3983b720018ccc4a7db7e5bebf7ef9d94f30d1bfd3e586f95de4cc28`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 15:50:54 GMT
ENV JULIA_VERSION=1.6.2
# Wed, 25 Aug 2021 15:50:55 GMT
ENV JULIA_SHA256=380115d80e2f0bebe1885b80f67cf9330b659722f50608495962ab3a00e02977
# Wed, 25 Aug 2021 15:52:44 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 25 Aug 2021 15:52:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94e38c9a52486d45b983874c16e4ed2cafc1e0cda7cc4c34b832c42c4aa5635`  
		Last Modified: Wed, 25 Aug 2021 15:59:13 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd8c9e65c9771361b2f16afa924651e5f43bf39b8e83ccda8e8623717457cfc`  
		Last Modified: Wed, 25 Aug 2021 15:59:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a4951480d359f624d56248546b7283d8931f9745cf1880c5b7d666596ce99a`  
		Last Modified: Wed, 25 Aug 2021 16:01:32 GMT  
		Size: 133.5 MB (133478330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2eaf7364d1b3bf7c05799542202797425a8c379b6c2efdcc765132815f7054`  
		Last Modified: Wed, 25 Aug 2021 15:59:14 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
