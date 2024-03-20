## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:2008837c52de3bdf65d226e6286551bfc85a85fdb1e11295a143303a22809231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull julia@sha256:cb54b9ab28a89c67d152546178472eccef050aeaa3d2e988bd6f713d3aefd9b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2209495990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6b47f8edf39f646801aad1975ac0e6e7fdf201f10cc5880122268a32b3365b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Tue, 19 Mar 2024 22:57:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 19 Mar 2024 22:57:21 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 22:57:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha2-win64.exe
# Tue, 19 Mar 2024 22:57:22 GMT
ENV JULIA_SHA256=acfbe50c378e3e0d6dc967525b5886edd5ae61ef3de85130343db378dfe88b0d
# Tue, 19 Mar 2024 22:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 19 Mar 2024 22:58:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d637cfff1b3d01ab2b5c2d275647b131469902318b1096779527dc4c166c92f`  
		Last Modified: Tue, 19 Mar 2024 22:58:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a83ffb9a5dd0011e2afcc146a3baf0468b5d2301fbeda383b43c4e20ca4103`  
		Last Modified: Tue, 19 Mar 2024 22:58:29 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da75395b5c3c24adf6d3a2b40e0abecdd8486ca9099f7b3f7e4263d64811866b`  
		Last Modified: Tue, 19 Mar 2024 22:58:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a234d7dc71ab909b21a8d7181557a39a6d8df8753ca7c0a0dd4c3afdafdc479f`  
		Last Modified: Tue, 19 Mar 2024 22:58:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36503805d95264323d243c5c1cb42d34ca3a50a88ee5d1859728ed9ee123460`  
		Last Modified: Tue, 19 Mar 2024 22:59:01 GMT  
		Size: 252.0 MB (252030519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e95cf5984ec86312c84234514711dfeba136da49603c2fd0330095ead86048`  
		Last Modified: Tue, 19 Mar 2024 22:58:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull julia@sha256:efb5a6919652a8eb85108e4da430cbdd7f35ae34f3e78a57eb48fe7b2a3e24ca
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377144356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4b41f87973a780c8a3777c31b7f53445f6a68e828eeb78d3ac5261bf96e45e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Tue, 19 Mar 2024 23:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 19 Mar 2024 23:04:19 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 23:04:20 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha2-win64.exe
# Tue, 19 Mar 2024 23:04:21 GMT
ENV JULIA_SHA256=acfbe50c378e3e0d6dc967525b5886edd5ae61ef3de85130343db378dfe88b0d
# Tue, 19 Mar 2024 23:06:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 19 Mar 2024 23:06:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679598d82b5034af97f421afba74d74d280902474c79a09de64a4d4932a114cb`  
		Last Modified: Tue, 19 Mar 2024 23:06:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685ffb5870e30e0d6e4da03b2989ba43d4262f9e7565b66693d06551ebe023ed`  
		Last Modified: Tue, 19 Mar 2024 23:06:37 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb8a8ef21b5b250e969ebb14ac99ae3329f516af367f4a3b6b868bb45e969c0`  
		Last Modified: Tue, 19 Mar 2024 23:06:37 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087c96a0f5b03b6909ed109269436871194ee6c09c5e8cd839f730b149698231`  
		Last Modified: Tue, 19 Mar 2024 23:06:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e7d9a209b998b5e71f42c45d40daed29b8d9a36c57039849d0935afda561ae`  
		Last Modified: Tue, 19 Mar 2024 23:07:10 GMT  
		Size: 252.0 MB (252037928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245f530187c70c384bacfd6ab4385ae3159b7187ed8451b128fd4bb0e6954b41`  
		Last Modified: Tue, 19 Mar 2024 23:06:37 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
