## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2ac7554e5b5c15a45430f1edd838a3be1f2160f88756175afba780ccc3d317fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

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
