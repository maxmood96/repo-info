## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ddacff95d5a2831fa2c5a5eb65fb1a7f62dee734d815f338619d9339cc22dd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

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
