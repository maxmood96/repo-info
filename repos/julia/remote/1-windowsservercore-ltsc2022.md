## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:266e10f006f04e0782bbdc6688653bd3aa15cc071205613dd04a3fa985e39f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull julia@sha256:aee0796b9525fa761628be4aac1e11a1ce4b8501d97ce782b3f9734c285af7cc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299979770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef31b149eb365d311201679c9b698c6cc9e284f02a02b69f72d0c597e817265`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Thu, 06 Jun 2024 00:56:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Jun 2024 00:56:35 GMT
ENV JULIA_VERSION=1.10.4
# Thu, 06 Jun 2024 00:56:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.4-win64.exe
# Thu, 06 Jun 2024 00:56:36 GMT
ENV JULIA_SHA256=c1b659abc90991dcbdf461f33cae483501da736fc223c11d4c51f337338ccb21
# Thu, 06 Jun 2024 00:59:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 06 Jun 2024 00:59:05 GMT
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
	-	`sha256:49964c91af65229edbe7db662b05a9bca98ee40d811d8844b54894fc364abba4`  
		Last Modified: Thu, 06 Jun 2024 00:59:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d919dfbf2c99cc13acb07a07734945cbb019709f6311cef2caefebf4d605b9`  
		Last Modified: Thu, 06 Jun 2024 00:59:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87516a2ce4f94c113e03a6d7c67b45b7ea997d7ba7f7dbc7588280477b92aa61`  
		Last Modified: Thu, 06 Jun 2024 00:59:08 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641cf305cadc8be1c23f3e48c38c56f698629d7e0266c3e020a4a03917ae6459`  
		Last Modified: Thu, 06 Jun 2024 00:59:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cf01ab23d2799dbab415f26772326cfed4d710cbab4b91da80733f42cbe42f`  
		Last Modified: Thu, 06 Jun 2024 00:59:31 GMT  
		Size: 187.3 MB (187301929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f63e729ed0745e5ba4e2838613a98f2521c3b0cb586ae820f9c613ba16945`  
		Last Modified: Thu, 06 Jun 2024 00:59:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
