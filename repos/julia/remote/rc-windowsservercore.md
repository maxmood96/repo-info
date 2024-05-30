## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:53ccc5e26e2e470554d3f630f79cd60c651c26cab4283bc964cf68db8273864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull julia@sha256:7bb517549663c77636253ecb1c72a278c4f0a44a6173db46cd8f64c4c6407371
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2361503042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842fef3bfff5f8ce36dc74bffd585f80014ac65a570b564eba334d7c1d68e12d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 23:00:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:00:47 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 23:00:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta2-win64.exe
# Wed, 29 May 2024 23:00:48 GMT
ENV JULIA_SHA256=e6d27f8a5819fd9e63ecb4ed19bed8a0c1ab719a5a6cf0f772c240eb44b46d68
# Wed, 29 May 2024 23:03:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 29 May 2024 23:03:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d78b7f65c77fd383010049b6d9456047b15237d2bce77c4df9c5ad53dd9ffb`  
		Last Modified: Wed, 29 May 2024 23:03:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b706afd37a6483d776469b487d997734ac848ab4a96dbe0dfbc3602295a48a`  
		Last Modified: Wed, 29 May 2024 23:03:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61698989f3f5a734d0a6539c3fe38e893df9dd5ab23b94cc042232ff85717001`  
		Last Modified: Wed, 29 May 2024 23:03:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d842bb0d31a98829df0a067a3e4c3926a1bac0306811f8d568e748dad3c92`  
		Last Modified: Wed, 29 May 2024 23:03:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2fa30a0343f67511930d82d1eb6c084307104569ed1b05278ffd5462c7b30`  
		Last Modified: Wed, 29 May 2024 23:03:39 GMT  
		Size: 248.8 MB (248825208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc56e015c8c912f99efe67f2aae70520e3fdf4bfdcfcf1aed93515ca37aef5a0`  
		Last Modified: Wed, 29 May 2024 23:03:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull julia@sha256:ac6440e38db5ef8ee87e1446d99d6a70dd8a821920e7ce2475a311ff5506497c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428708449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795ebe1326119162288862fda3f7bbee21d21aed995ec3c5058245f62340eb0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:00:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:00:48 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 23:00:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta2-win64.exe
# Wed, 29 May 2024 23:00:50 GMT
ENV JULIA_SHA256=e6d27f8a5819fd9e63ecb4ed19bed8a0c1ab719a5a6cf0f772c240eb44b46d68
# Wed, 29 May 2024 23:04:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 29 May 2024 23:04:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fb78f061fe3d75b9fa79f36c2c88995a8a98fa46d662a7e44427420400fcd3`  
		Last Modified: Wed, 29 May 2024 23:04:25 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de627fae923915a4c0bd322ad1fd077c3ee71b457606013a54b2c94416f392f`  
		Last Modified: Wed, 29 May 2024 23:04:24 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441200e8b91e19f181df688d20e6715f6cf1a0f696019d9e13e52aa69b01b9c9`  
		Last Modified: Wed, 29 May 2024 23:04:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a98243968ca590e29a12c9dc8803d01e518ef98bfbcff97b9b55b846c53959`  
		Last Modified: Wed, 29 May 2024 23:04:24 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca027bc80eb1d89357d4c5d575aec3e9107cfd0ec4443fd4078ce256a522c683`  
		Last Modified: Wed, 29 May 2024 23:04:53 GMT  
		Size: 249.0 MB (248990482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73a736e1176526874f3ddafeae72f517bb500b7bd7e47c0982e45a46492abb0`  
		Last Modified: Wed, 29 May 2024 23:04:24 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
