## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
