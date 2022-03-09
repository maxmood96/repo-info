## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6f3d95d99812b9e062bbe6c7e73494addf7e554a919d6984eadb1b570b8379c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull julia@sha256:7cfb2cc4561d4ca54065c56965416d8180cf40094e797c56789d551ae2044463
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2366244820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a123318eecedfec81d3d41c90a275a47074c7dbc73962c26fcc83935364ce4c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 16:15:07 GMT
ENV JULIA_VERSION=1.7.2
# Wed, 09 Mar 2022 16:15:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.2-win64.exe
# Wed, 09 Mar 2022 16:15:09 GMT
ENV JULIA_SHA256=bede21e00130c2dcb6973a968b7ed43c35d69712008a95bb08d5536d3c9e2585
# Wed, 09 Mar 2022 16:16:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Mar 2022 16:16:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56484681fe99e395896c51ecd1c3050e4c6475ffc6f4aea9c87fcb8df550424a`  
		Last Modified: Wed, 09 Mar 2022 16:26:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d20bb5b3ccb9177b37c24c49ae0e97890c53397cca743a803ac848c8b1e7f67`  
		Last Modified: Wed, 09 Mar 2022 16:26:53 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac70c3ee61911e53aaf49b4a6554d0845a0015f71285e31176cb1e81df8a5b2`  
		Last Modified: Wed, 09 Mar 2022 16:26:52 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f629a8388d6f9d2bc984122b5ce790445703cd39c4a828f2f7e4ce6c1064d2b`  
		Last Modified: Wed, 09 Mar 2022 16:29:24 GMT  
		Size: 145.0 MB (144990635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41425d0532b9ed67330ff214a14908a93b2e7fa7027eb9d0c5260bd05b48c8eb`  
		Last Modified: Wed, 09 Mar 2022 16:26:52 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
