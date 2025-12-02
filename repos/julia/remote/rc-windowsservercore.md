## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:fc0a6ac8bd93e290c005b0918d55f4d5e7ff4bda4de3ae6562c298371e88295e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:rc-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:561937bf6e37457b2aa4707c3ff040b3dea59225f94d30532553fcf692f8f7c8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869007100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037ba1986027ea1cb6bec88fe9db7627cc36e62ee7af73e9947a5dbb92d20f67`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 29 Sep 2025 17:52:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Sep 2025 17:52:22 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Mon, 29 Sep 2025 17:52:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc3-win64.exe
# Mon, 29 Sep 2025 17:52:24 GMT
ENV JULIA_SHA256=4700e3325fe8d8c8f209fe09aa95928ff1c65b45fdf2968124bb143c5c59aded
# Mon, 29 Sep 2025 17:54:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 29 Sep 2025 17:54:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Sun, 09 Nov 2025 13:33:08 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc1e52f9bc29ce53d26b523c04988f69995788c22f43dc5eef117a6b5b69ed2`  
		Last Modified: Mon, 29 Sep 2025 17:54:41 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d667d6ca0ce99f83e02ab6dfd13017d89a62db952a3adbfacd25b741d40cbffe`  
		Last Modified: Mon, 29 Sep 2025 17:54:39 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f97168be5efa1c6f5fe3c5d033f6b92569eec1324b72371efdfb4cdd9c5688e`  
		Last Modified: Mon, 29 Sep 2025 17:54:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1313b88e9837ba5ee3a39b8cdf814429858a1118b5ef34cd7311d90b9ea2e5`  
		Last Modified: Mon, 29 Sep 2025 17:54:39 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c7cc3abd0694dc02e2d589325c8e7607e467a44e89089519146fe297448d5f`  
		Last Modified: Mon, 29 Sep 2025 17:55:25 GMT  
		Size: 297.6 MB (297560786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5a7a1f6a11c973fa364d5ab8e67ee983e78caeec93e2994dded506010409a4`  
		Last Modified: Mon, 29 Sep 2025 17:54:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:6b158b2ae86f1a22218959e920b5e0c3da0086252c7465f0f99a8eaf3748c42d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579659431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e728f95378332db793877542399afa53751f58ae05ec4d1606acad128a90a9`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 29 Sep 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Sep 2025 18:14:13 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Mon, 29 Sep 2025 18:14:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc3-win64.exe
# Mon, 29 Sep 2025 18:14:16 GMT
ENV JULIA_SHA256=4700e3325fe8d8c8f209fe09aa95928ff1c65b45fdf2968124bb143c5c59aded
# Mon, 29 Sep 2025 18:18:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 29 Sep 2025 18:18:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Sat, 08 Nov 2025 21:28:12 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3662dfe36956d8cc7d770032f6242679aa97aa455b257e51284077f5c991083`  
		Last Modified: Mon, 29 Sep 2025 18:18:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ec2a6551600fc1aa44df9306e276fa86ab75e73277994e82d219f3ef0149ee`  
		Last Modified: Mon, 29 Sep 2025 18:18:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66436db09c21c6c1eb91810bd524cac80b897e605d8577712c23980ab21b317c`  
		Last Modified: Mon, 29 Sep 2025 18:18:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969246bc70379a38f812334714440f7bcfbbf827957a92dc2c4544f2d7211783`  
		Last Modified: Mon, 29 Sep 2025 18:18:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a23a30b61012f7a59fb4d441266b7a8178c9bca3ea1af1265c37937cba86e0`  
		Last Modified: Mon, 29 Sep 2025 18:19:30 GMT  
		Size: 297.5 MB (297507925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fd026e3d12b4a1dfe27d3afbcb7966f972c49e4ddf6bb34827fea1990529c3`  
		Last Modified: Mon, 29 Sep 2025 18:18:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
