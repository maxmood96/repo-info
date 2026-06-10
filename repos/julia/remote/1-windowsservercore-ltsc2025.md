## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:f6f82ee53d7503ec55d1d17b602e155b97717139ef4411c19dd21caf9075ee33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull julia@sha256:bf36ac6b6182557f7a0c064ce6229aad88f2ca27c7792b03522b561ee57685c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567652353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa7831bf80a77063592948e68dfa24619c78839978a9be8e36e9599241664a9`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:12:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:12:29 GMT
ENV JULIA_VERSION=1.12.6
# Tue, 09 Jun 2026 22:12:30 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.6-win64.exe
# Tue, 09 Jun 2026 22:12:31 GMT
ENV JULIA_SHA256=de2d50f23995d71c224423a4872673a4e9be2c9676fc975cd90b25fc3a5e6cb6
# Tue, 09 Jun 2026 22:14:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:14:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd9775be4031937efdc97f503b8e8073012c6d3367d79761e42678fea5e5a9f`  
		Last Modified: Tue, 09 Jun 2026 22:14:23 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc529054c6f05f098eb80d65256ecaabe1c8f8992cc8348daacca448426f5cc`  
		Last Modified: Tue, 09 Jun 2026 22:14:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dd194f4ea7872fd832ecb11b6aee88ae0958d67c7439b3515e9437eb0c8c25`  
		Last Modified: Tue, 09 Jun 2026 22:14:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6eda80a14ced8c1a437f00fd128527688198c7d8e5dc194a11f88a35dc3d81`  
		Last Modified: Tue, 09 Jun 2026 22:14:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba511def2ddf9da58c87f0d2cb453a946d07f58b607146a1523d49a85b254fb1`  
		Last Modified: Tue, 09 Jun 2026 22:15:01 GMT  
		Size: 288.5 MB (288502848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29692cf3c5f0828d70b5ea6abadfd0b057b3d138ac1c8d0488b45240526c3d14`  
		Last Modified: Tue, 09 Jun 2026 22:14:21 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
