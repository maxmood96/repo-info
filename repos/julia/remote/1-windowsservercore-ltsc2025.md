## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:a161b92b2fd12b8687ecf37fd4578650c429e8298f916fc28c7e911d4d530085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull julia@sha256:8658f69f6d59880fca31dae926d151e3ed26784ac1ea67e0ff9196c4e893830d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3659811964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79abee34cfe2f0313f5438cf73abfcd88b4555b3a3b65cc4fa67c6d253f9e1d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:52 GMT
ENV JULIA_VERSION=1.11.4
# Wed, 09 Apr 2025 00:39:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Wed, 09 Apr 2025 00:39:53 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Wed, 09 Apr 2025 00:40:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:40:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be99445d9e85df6142e017d8f20de89b5b05da85013755f0dda53b36907bc`  
		Last Modified: Wed, 09 Apr 2025 00:41:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee309b52e771416f0192fa9a02533a1308fb41e0210a0ba396ad998ec54639a0`  
		Last Modified: Wed, 09 Apr 2025 00:41:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62f921ed34ffffeed19ff2ef7c520c96922501e73b9dd17970021b8c5cf60c2`  
		Last Modified: Wed, 09 Apr 2025 00:41:02 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13776b7c46a870c665f814dfff1eca8f122144a064e5f124fe54d3ff0746e2f8`  
		Last Modified: Wed, 09 Apr 2025 00:41:02 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5748e633b1e267619f88a05d48dd8eca6744e261cb7f6e5888fdc8aaeeae00`  
		Last Modified: Wed, 09 Apr 2025 00:41:42 GMT  
		Size: 265.1 MB (265125951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c49dc5ecf326cbf15729bb0c7a1890c25f0906fbbfb0615263d67519ccd61b`  
		Last Modified: Wed, 09 Apr 2025 00:41:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
