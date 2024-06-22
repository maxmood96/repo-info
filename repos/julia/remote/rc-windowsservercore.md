## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:e5fecaa0823ed481ca6988579d73e2730ff14cf7a2bdf4271b07bafddd95c937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull julia@sha256:350321555df286190b404c3b9de5496f30be61193078f1d3538cb1b295add6d6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2367021510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820df9d25157666235363363f6832b785314fc7130b2d8db7246738c2dbda92e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:04:56 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Sat, 22 Jun 2024 00:04:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta2-win64.exe
# Sat, 22 Jun 2024 00:04:57 GMT
ENV JULIA_SHA256=e6d27f8a5819fd9e63ecb4ed19bed8a0c1ab719a5a6cf0f772c240eb44b46d68
# Sat, 22 Jun 2024 00:05:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 22 Jun 2024 00:05:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ccf296c11c54ced1fbbafe3c2d2cb084fb2be16cb7fd3c92c577b2db9206ae`  
		Last Modified: Sat, 22 Jun 2024 00:06:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1e8090c700c2be35aab82a039f9adda83014d50c09832d5a61d05b8beea6f0`  
		Last Modified: Sat, 22 Jun 2024 00:05:59 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55954a7eb731f93875b3bb655c781a0e127c204efe21421c6251f557f1ebd2b7`  
		Last Modified: Sat, 22 Jun 2024 00:06:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1728f9546b70de39476bc172fe3bb243aa87a2bc75b304e175307869b344cb9`  
		Last Modified: Sat, 22 Jun 2024 00:06:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6393eff90a0d26d6446e914e1879a4e927a05fa7dad7f7fd9aae2e999be6f73`  
		Last Modified: Sat, 22 Jun 2024 00:06:33 GMT  
		Size: 248.8 MB (248824787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b147bb5573fb99809b0ca040e4f194b115ca7a7c4d653c8aa913645125663db2`  
		Last Modified: Sat, 22 Jun 2024 00:05:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull julia@sha256:aa9e71793ca1ed74c38727635776de97077aababb2a381758efae0df5cfaf6dc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2469627943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d69a10cf626749fefb8f490b3102351231e6d385cea547f0cbd2d7e2bf218`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:14:05 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 12 Jun 2024 18:14:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta2-win64.exe
# Wed, 12 Jun 2024 18:14:07 GMT
ENV JULIA_SHA256=e6d27f8a5819fd9e63ecb4ed19bed8a0c1ab719a5a6cf0f772c240eb44b46d68
# Wed, 12 Jun 2024 18:16:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:16:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f2848b507d340046821201398db87834f5d7a8d7e418f888f3a904e4b5afed`  
		Last Modified: Wed, 12 Jun 2024 18:16:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03878b5efd7a4a26ac690ef352963e31ca6398ebf8323539ed7732affd47507b`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc6f58c70479f78d5a9c19f8c725ca3d96e58f6ebd936977e9b958c437584f7`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71f6834e00a050a5aebc0b88a91b19df0a4104d7af64849734be80b8f351e67`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206ece9174ecfdd1698fae1fedf5c2bf920a2de5121235bf20a00a16aa8f22a9`  
		Last Modified: Wed, 12 Jun 2024 18:17:03 GMT  
		Size: 248.9 MB (248940285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88ab638f6b0150e77b9a23480dbe9d498b670181a6c91f5c01c3c26ee2e2288`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
