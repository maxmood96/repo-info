## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ce31648f7edcdb3c172fe160855a43dcacb1bb2e008284b0a4b807139aba2a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull julia@sha256:7fe0b9276a9aa9dcaf43fe3e82c7fbe8ccdb4c30aa5bf37456b1aa172e9ec5e1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3683461129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348b648a403dadd57b09da223a1e23b8f6dad372763a0d3cbb8688bad7caba5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Tue, 13 May 2025 20:04:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 May 2025 20:04:23 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Tue, 13 May 2025 20:04:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta3-win64.exe
# Tue, 13 May 2025 20:04:31 GMT
ENV JULIA_SHA256=1aab913a2acd82a1eebaa63e958d3d5741306aad93ac663afcee5791691fe96b
# Tue, 13 May 2025 20:05:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 May 2025 20:05:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98f25ca18b5e7eca835fc60353e3de9054c1464e4055147c25a4617fddc1e1d`  
		Last Modified: Tue, 13 May 2025 20:06:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7ad62e3001817beaf1c5a7a03a35587f7dc2048284ba1ed53f6f21094895f`  
		Last Modified: Tue, 13 May 2025 20:06:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dae94d922926c70ecffc5bdac0ff758022b778f5067573b5bf2c12642828fbf`  
		Last Modified: Tue, 13 May 2025 20:06:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c1174b6d0bddc7ef320d014b267914e4ee53cd85162180815c9bed2e85b9ba`  
		Last Modified: Tue, 13 May 2025 20:06:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869edf2a0b79e5215a2dd482d23d10ff5a3c08ca1a03fc0b884371554f8a7810`  
		Last Modified: Tue, 13 May 2025 20:06:46 GMT  
		Size: 288.3 MB (288293275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b54d8a0839e3b2cc8eff229829bd57ec5153cc2fa2e59795bad1d628698da`  
		Last Modified: Tue, 13 May 2025 20:06:00 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
