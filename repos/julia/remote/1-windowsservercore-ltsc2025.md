## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:0f687e5f28eed3e10f1c466bafc3979e367a5c276f3af3ab0811dbc32826dffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull julia@sha256:b32d6e4211afdb50c4df071df0bfacb06076414fd926e80f64a67dffc55a17dd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369698117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49de463e96df86af3597eac169a738a4190366fb246c4423cb01a953e5bff5c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 13 Apr 2026 23:51:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 13 Apr 2026 23:51:58 GMT
ENV JULIA_VERSION=1.12.6
# Mon, 13 Apr 2026 23:51:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.6-win64.exe
# Mon, 13 Apr 2026 23:52:00 GMT
ENV JULIA_SHA256=de2d50f23995d71c224423a4872673a4e9be2c9676fc975cd90b25fc3a5e6cb6
# Mon, 13 Apr 2026 23:54:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 13 Apr 2026 23:54:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077fdf2334dca0a37a41a024f576999fa4fd25a235de0d94de95313f70dadb5c`  
		Last Modified: Mon, 13 Apr 2026 23:55:08 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72db3495ec4106c52a6d815e8898f61bd05c0c55dd2c117008b4e3c1b7b197e2`  
		Last Modified: Mon, 13 Apr 2026 23:55:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcd0008b8188281bf4010672ee958f1f267f8b1d5e7f9d60bede8cc1b790e83`  
		Last Modified: Mon, 13 Apr 2026 23:55:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f352124fa7263249ca6c6f60436993e587ae6708b9e75635ee13ef24c1b39c`  
		Last Modified: Mon, 13 Apr 2026 23:55:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ab10c0ba0bcc1a04e6f50b24ca5990d6142053f6cd34e501c07e4e45e54609`  
		Last Modified: Mon, 13 Apr 2026 23:55:49 GMT  
		Size: 288.5 MB (288495544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46a195175a3d83b2ef170dd73dcabe0da712404a9ab423a04ea86479b5d9b2c`  
		Last Modified: Mon, 13 Apr 2026 23:55:07 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
