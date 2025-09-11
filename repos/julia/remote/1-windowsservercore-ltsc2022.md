## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:49b4a98616c12843bfd71c8f6899db26dd79171105f902efda0f77a5d216585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:794f5e6af132b10b705d23424d28f5a31b888a0587cea0780d17a574bf8929c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568064260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafd798e43ab65d26c1dd812eb83db75c98d02f3a772baceed40bc20f83edc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 20:20:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:46:44 GMT
ENV JULIA_VERSION=1.11.6
# Wed, 10 Sep 2025 21:46:44 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Wed, 10 Sep 2025 21:46:45 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Wed, 10 Sep 2025 21:47:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:48:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe60f506e392727a189c473ed3077c57345b082b3f502c4e12299121d8a339`  
		Last Modified: Wed, 10 Sep 2025 21:43:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765abaabd19fafbee9cec7b94b9e272503ba42fffcf424af1415e92a02d8866e`  
		Last Modified: Wed, 10 Sep 2025 21:48:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f65d69492f5398c8fcde6196adb3b29743275e5d4048b0e62782197b3c26f9`  
		Last Modified: Wed, 10 Sep 2025 21:48:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec697a1b682605e610356c6cadfdf098503633a8d040adca5506991f575f5a46`  
		Last Modified: Wed, 10 Sep 2025 21:48:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0489fa8c062746162be21c22912f46b029f071a1e15ddde8fddbcede540c33`  
		Last Modified: Wed, 10 Sep 2025 23:03:22 GMT  
		Size: 285.9 MB (285912762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d185d2ed18d6d23e2ece173c2bd82cd2e3fea7bfc459883a8ab75bfbd9983162`  
		Last Modified: Wed, 10 Sep 2025 21:48:56 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
