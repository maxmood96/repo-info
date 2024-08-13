## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:b172e5e8d4974f9208523098d37bf0809f09e5643898155177736a81d728ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull julia@sha256:a077cc9b1a92355746f907bae837e6151b39dece74065bd1e844d8cfc6c12368
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2390592804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b65dc26c4d19554c548ab325a00c16a5a2399864a60fb0f96479fe8a0d81b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:22:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:22:25 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Tue, 13 Aug 2024 20:22:26 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc2-win64.exe
# Tue, 13 Aug 2024 20:22:27 GMT
ENV JULIA_SHA256=5c9b27f41094a3458973eeede7ace2af4c2fadadbc7f30b700ab8cf089641d15
# Tue, 13 Aug 2024 20:23:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:23:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeebe7dcba53a07615c57ffa0b6f7cc6ef78f84abb8b4c693cc12ce69ebb144a`  
		Last Modified: Tue, 13 Aug 2024 20:23:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dd7e4dc32ee62c1ef07e207d09d7ffb898e5cce656a319648478f8a9eaa19e`  
		Last Modified: Tue, 13 Aug 2024 20:23:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d03ca65b4f7dc9d051d4a1e1c9cf16adec3c06a94f382ae4f5400911af53a83`  
		Last Modified: Tue, 13 Aug 2024 20:23:36 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0ee4087d9d6fd6940d9faeb5887d5deb58fa6a6f7fd1b01c95f6bfe6322067`  
		Last Modified: Tue, 13 Aug 2024 20:23:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac99ccc17fca8c64ca39e38de78b5f34fc271f25bfb065c9a71c1a3364451c0`  
		Last Modified: Tue, 13 Aug 2024 20:24:07 GMT  
		Size: 248.8 MB (248821420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c0cb0920f19b5b1f58ce72f18ca8190977576bf1dfdee573c2fb0bb31d8528`  
		Last Modified: Tue, 13 Aug 2024 20:23:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
