## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:7f6b55b8c705e77169a889873fc3172c294df75034b12e3738881072903ab75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:8b4baaf9bc674fd57f7f2f240245dff91f7ab8233be37f201b21e64207449e9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1786538943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99481f45311a8c007ff89cc3f1f960290ede160b3d570cf62a9a3e581c04b8ae`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:01 GMT
ENV JULIA_VERSION=1.12.0
# Tue, 14 Oct 2025 20:42:01 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Tue, 14 Oct 2025 20:42:02 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Tue, 14 Oct 2025 20:43:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f2742f3144bf637c948400edbc59f380821c3a8b3f6172bcf5adec6fe214c8`  
		Last Modified: Tue, 14 Oct 2025 20:46:40 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c33cbe0fd453c7205520cd5b18ac3701200c285e82f4ed2c2db87ae1f9cbf30`  
		Last Modified: Tue, 14 Oct 2025 20:46:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2ef29c77d17e2ff3520e338048050be75f05590356757a7ae9bab349719d25`  
		Last Modified: Tue, 14 Oct 2025 20:46:40 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288c4ab060c6ae4faf59d2b96a0c535f9c201675f9e29727dccb45c1225db923`  
		Last Modified: Tue, 14 Oct 2025 20:46:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36635ecb6eef0a314bb4795c47221b7a8c8d6eb532b21b784a1d6da1a771adaf`  
		Last Modified: Tue, 14 Oct 2025 23:03:04 GMT  
		Size: 297.5 MB (297513208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f10f0c70511c2c8dea245af603caf0a13257d3497898d045b4783d5ac4b14e`  
		Last Modified: Tue, 14 Oct 2025 20:46:40 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
