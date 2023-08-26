## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:9e1a0ee9f108addcd617a42f7dc07a290ac073db22649a263834fbe0e05b944f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull julia@sha256:6f84553294fb90710609622d4f829462d89ae25d0fe26f8125d05d4392da3897
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177248053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db393aaec81277578d95e4dc782158b9e6da44389b7fa4ba33c914a9818cb135`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 26 Aug 2023 00:16:46 GMT
ENV JULIA_VERSION=1.10.0-beta2
# Sat, 26 Aug 2023 00:16:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.0-beta2-win64.exe
# Sat, 26 Aug 2023 00:16:48 GMT
ENV JULIA_SHA256=21fcab0815ce738bb268daa154dccbf0532b7c27196586ce677d43164114474b
# Sat, 26 Aug 2023 00:19:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 26 Aug 2023 00:19:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d0381b7df0d91b892d604b4d43fdfe1b55a00fb6131bc4c886f332528a3366`  
		Last Modified: Sat, 26 Aug 2023 00:25:22 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdf1c547752ba7eabdc8d03ffbb3f8f2443baf14ceb9905a040949053c6fc32`  
		Last Modified: Sat, 26 Aug 2023 00:25:22 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0879d3a3c36a90c775847740af299deb2d3d7fb61919c77d8e7a6105039f084`  
		Last Modified: Sat, 26 Aug 2023 00:25:22 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85d9967671a58c967766d7528e88e22f21088923a5fb07c54117d340d33b85b`  
		Last Modified: Sat, 26 Aug 2023 00:26:03 GMT  
		Size: 181.3 MB (181285569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d4596cd290efb34ddcaa3bf6bcebff4c7fbfc5b3754e6fd4c67e2032525bb`  
		Last Modified: Sat, 26 Aug 2023 00:25:22 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
