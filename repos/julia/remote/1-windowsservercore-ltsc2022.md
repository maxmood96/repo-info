## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2a0dd1446d94fdbffd2075628d86db8741612040d64d4a94e23b42b57ab2f462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
