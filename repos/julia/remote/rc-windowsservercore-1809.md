## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:610eec3be43112db8cd6abda26900052760c0a670fe9030c0944585b221b0f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull julia@sha256:e87f65e4ae843949fdb7b111836aa61baa9be549855b5547b89f0f6b6b96df80
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2497474476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bdbbfce3254360fb6216ee173a0d386973e6452a5ffa9546aacfaa06549c97`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 27 Aug 2024 19:56:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 Aug 2024 19:56:03 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 19:56:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Tue, 27 Aug 2024 19:56:04 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Tue, 27 Aug 2024 19:58:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 27 Aug 2024 19:58:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e41993097840a6f84ef1f126e6db081e1a8ad55f7f89d4b157382cde7a180fc`  
		Last Modified: Tue, 27 Aug 2024 19:58:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0115fd5fa2c2d05059d08ecaabb6269d74d6d2c4b5860f85c7c8e5481f29be6`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c12cc15a7f0bb45833f020c942e01d783cee0547462f94ad360e05e96e79c2b`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5d1e2c8d818160dd29c0e37dabc52855165e6d35c6732f5a686adefaeda787`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76898a9dd96fe3582db7c090ba6f3eadd4f8198f89a681311600dc65a6cdfd60`  
		Last Modified: Tue, 27 Aug 2024 19:59:20 GMT  
		Size: 252.3 MB (252264784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c691d0511554e576cfad409beeff1511f20ad67e774025923ff6b2d3752c46e2`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
