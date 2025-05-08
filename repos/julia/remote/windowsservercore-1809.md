## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:9ed2d3d44b13e9e39c9cc3c06568f58ecb20843b20a0c540828eeeca58662f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull julia@sha256:9ba8e4bf5b80cba6e085938c456369ec708aa29ae04547cdc26abf3b631d761f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2450958227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0da57bba8326d10f261d415e0c24a695778160c2f5090c3eaa82c8af680b38`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:18:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:18:10 GMT
ENV JULIA_VERSION=1.11.5
# Fri, 18 Apr 2025 03:18:11 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Fri, 18 Apr 2025 03:18:12 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Fri, 18 Apr 2025 03:19:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:20:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54213492d1ccb0a74c2e468a68842e2124749c91e3d89efb970b27bb0020b7f8`  
		Last Modified: Fri, 18 Apr 2025 03:20:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1568b8c0a79a85cfd343807fdc5e8f5f78a1efb57b8b8183569f0f121b8fe5`  
		Last Modified: Fri, 18 Apr 2025 03:20:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5756298203bfb944cbbe41b70eeab579ac6fb88365ca8b8819d8e752c5560c`  
		Last Modified: Fri, 18 Apr 2025 03:20:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24eb4eedd752d7942ab1530d283f631e1466d06317b3422e4d12c0a29edc506b`  
		Last Modified: Fri, 18 Apr 2025 03:20:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5b01f0e330a8fbd7807a0b2fda41ec381f870f8fbf368da4f4f6c56274e415`  
		Last Modified: Fri, 18 Apr 2025 03:20:40 GMT  
		Size: 285.4 MB (285425944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be41e1472572d7236a9a8fdb957e5a3c39aed05066f987ca4e379ca4af6f4`  
		Last Modified: Fri, 18 Apr 2025 03:20:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
