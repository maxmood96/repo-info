## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:1d708814186c71c95c8d8525af66eb54242f2b7d4bfc59b9806e7591b7fc79fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull julia@sha256:0aa63c8ca96d81f63de0a0471ef2da1ee1d7acb7f9b65187fbdd5270fb281d60
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3680701864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1841f2f2bb5f66d1127fdafd997001a285b193ca513118d0fa149cda4bdc35`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:13:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:13:50 GMT
ENV JULIA_VERSION=1.11.5
# Fri, 18 Apr 2025 03:13:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Fri, 18 Apr 2025 03:13:51 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Fri, 18 Apr 2025 03:14:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:15:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab14e22d25368528b64992f9624f23945b46c4d5a0feae35166e6bc296fd30`  
		Last Modified: Fri, 09 May 2025 13:35:23 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bea43a4aaeebc743c3a3ed0403cc7ef8971d8de413afaf9a50cb0883eb2ceae`  
		Last Modified: Fri, 09 May 2025 13:35:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66b992ef9b14ed9e141eb392ae9cb16af297cc967281ceefc4b63d99d3c0f6`  
		Last Modified: Fri, 09 May 2025 13:35:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20cdd82857f596cc0954a179ff7e1d6d837acc513367a74330988ec6accbb74`  
		Last Modified: Fri, 09 May 2025 13:35:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564e84314e2dcbfab64f54907f9a167efddc0bbb7cfca71576bd7943793bcf23`  
		Last Modified: Fri, 18 Apr 2025 03:15:46 GMT  
		Size: 285.5 MB (285533999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd2ba56d727f01934f3a94465629c2b8dba44580d245ae8379b5580d7d305fb`  
		Last Modified: Fri, 09 May 2025 13:35:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
