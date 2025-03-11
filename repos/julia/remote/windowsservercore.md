## `julia:windowsservercore`

```console
$ docker pull julia@sha256:558e56296c78e7898fafefc944345bcb81b21a48f6137d1b8c9a74322b32c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
