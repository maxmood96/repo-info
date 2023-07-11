## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6735b471620aab8591c86867da06da7cb3854873f3c6378617ed8231b25da9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull julia@sha256:297503be629108af47150072bdc10058e7a2597a07f57bc712c903fbd6c93152
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1936495149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee54273ada606775e724047aca126b3e4f6d562a878804cd71bf7df20c5ad4d6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 05:24:43 GMT
ENV JULIA_VERSION=1.9.0-rc3
# Wed, 10 May 2023 05:24:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-rc3-win64.exe
# Wed, 10 May 2023 05:24:44 GMT
ENV JULIA_SHA256=5cfee20b00591abb548ca32f4931e52284e831c783238cba72e6f9622bf5e76e
# Wed, 10 May 2023 05:26:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 May 2023 05:26:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ee77e7f722c72ac215618979bed51f46c4ebe51de7884d88c48f9f56402a7d`  
		Last Modified: Wed, 10 May 2023 05:36:12 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e12f92b628de863dc218ea970783be08040929f1226c92eb606598e303bcbf`  
		Last Modified: Wed, 10 May 2023 05:36:12 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2268398f2b4da6656bba250480dbc4d9afe0710c7dd7048d3ef4397b4f17d702`  
		Last Modified: Wed, 10 May 2023 05:36:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc917e5ca305e0309fa69f65d54acde424fb9672c4ed9c2276ce368b06b548a`  
		Last Modified: Wed, 10 May 2023 05:36:45 GMT  
		Size: 161.5 MB (161506582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a080808adaa4f1e75b16acafb18d52f95cf72961d297309d6749b17848bcceb`  
		Last Modified: Wed, 10 May 2023 05:36:12 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
