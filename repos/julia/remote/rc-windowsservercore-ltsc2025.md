## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:02cb9a734a85481557b1887bcfa45c68eb8039cd2211bf124ff12b34dc7ca4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull julia@sha256:6e31fa44bf3974bf59fcb40bdfda5bdd88a2ef259b38e6eb369fcbd4867b6c2e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2276022114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29c96c6a5764255cf1773e258a01a399c5458600e9e9440b8b0fdce2dfe4675`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:52:31 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Tue, 10 Feb 2026 22:52:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta2-win64.exe
# Tue, 10 Feb 2026 22:52:32 GMT
ENV JULIA_SHA256=bcba1c45109550ad6da10076aa32c7c40d83af41a751341b22bb0f3046111a11
# Tue, 10 Feb 2026 22:53:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:53:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c98dbe9f1f0558e249573b12845ab1eecd63a28b82c4d7dd0c89342195382d`  
		Last Modified: Tue, 10 Feb 2026 22:53:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0242f935fbcd68aadf1db4e80b23ad1b209b321707cfc42e605fe50f43645259`  
		Last Modified: Tue, 10 Feb 2026 22:53:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ddafa87c088f05e480c0c69461e9ebfbc8c3c55180c5f7048bcfae7f45ca69`  
		Last Modified: Tue, 10 Feb 2026 22:53:51 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1e19c133a288bc3493f988adf7d1f9b33558e2465c511a04e45668bcaa1429`  
		Last Modified: Tue, 10 Feb 2026 22:53:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738667e33cd971cb8330a8bfe0ae596794e429f0501841bc0e72102b3f1612f6`  
		Last Modified: Tue, 10 Feb 2026 22:54:32 GMT  
		Size: 311.3 MB (311255714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62279fc54d0141ccd426c3c459baa0bf4af599f01a15d83fe9166e341f833875`  
		Last Modified: Tue, 10 Feb 2026 22:53:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
