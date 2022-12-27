## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:41182a752937028aca8d9ef97d53721a70794940e827b76798857dff891d1170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull julia@sha256:29e6cfe8fa1eb690a8bc76a6fee936344bd8966b5ec5e7dbc8ba03b2d7271811
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2638723614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9fb4882bb61e5a68ba87fb8cb3bc9c814a62a4eec1decdf125598ad5199ea5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Tue, 13 Dec 2022 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 Dec 2022 18:18:30 GMT
ENV JULIA_VERSION=1.8.4
# Tue, 27 Dec 2022 18:18:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.4-win64.exe
# Tue, 27 Dec 2022 18:18:32 GMT
ENV JULIA_SHA256=e040e6cc0db89aee459a2b6e383de3af7fad3a3e6b030763c414c11c43326029
# Tue, 27 Dec 2022 18:20:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 27 Dec 2022 18:20:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb8b9a4ec3ca516cfaa44f64e80b1e3aaecdbde870177411ff046f81f991dd2`  
		Last Modified: Tue, 13 Dec 2022 23:51:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9111be8295d8827d4cc368bf4744ba376536b0fc0d9e35fb178ed68906f26c02`  
		Last Modified: Tue, 27 Dec 2022 18:24:23 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d025e72e8b5f856108c22502f61c794013b454bd38e47cdab9f31576bc71b75`  
		Last Modified: Tue, 27 Dec 2022 18:24:23 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b4be1d503aca77409938ee68f3b8f33f72514a2d4acbebcc803b4f9535bdbd`  
		Last Modified: Tue, 27 Dec 2022 18:24:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dc5a8ceb85a46e96d87aa84f1bd1f56124c987c9e91cd096ce90115f3d5f73`  
		Last Modified: Tue, 27 Dec 2022 18:24:59 GMT  
		Size: 143.1 MB (143053920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520f820351b1f8dcb56c8cc0ae21a51513a86f2fbaf72948b9399e88092cd61`  
		Last Modified: Tue, 27 Dec 2022 18:24:23 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
