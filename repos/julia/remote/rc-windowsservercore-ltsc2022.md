## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cecc091aca6ce2b30cf2e5d2608de60c57ae92ab7a82ea1c0a364a4581f08764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull julia@sha256:427c9320dba4aa62b3f4fa1090846ab7786fff2534de1978757a242edcbe1b7a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2252108633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bced71389e9a9e516d2c1020f49ce89fbc83b8c9a6a721563de4e8ce023f8356`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Thu, 11 Apr 2024 00:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 00:03:26 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Thu, 11 Apr 2024 00:03:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta1-win64.exe
# Thu, 11 Apr 2024 00:03:28 GMT
ENV JULIA_SHA256=a4bd6d9298d397963fbc97f3595fa080433960f3a6c50e8eede76f69b946aff8
# Thu, 11 Apr 2024 00:04:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 11 Apr 2024 00:04:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc9eb60ad5830f879f35bfa03013b24de88977ace126b6d32b425edd2f487f5`  
		Last Modified: Thu, 11 Apr 2024 00:04:44 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd96289ada30494c2626fbd0da3abb55113aca661c5a5cc69556edcfff577037`  
		Last Modified: Thu, 11 Apr 2024 00:04:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb809da2e129c629c4f0f441a762c5db0bb8220e2e65e974491f7b106d2d51d`  
		Last Modified: Thu, 11 Apr 2024 00:04:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ceb27c6d31eb062baab450e78f0e29b1fb9c174bbda4ddcd2738ce069324b4`  
		Last Modified: Thu, 11 Apr 2024 00:04:42 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac3411e21e83915f472e2a8ea481f7b4f1490767539ac6602a74c972ee55d3`  
		Last Modified: Thu, 11 Apr 2024 00:05:15 GMT  
		Size: 252.7 MB (252728512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896a3e36be362a7d20c2765a079f41cb55a85f0d3a5b58b96fcf216b850dc27f`  
		Last Modified: Thu, 11 Apr 2024 00:04:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
