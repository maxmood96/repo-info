## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4de4115b7605a43e5d507ce0cc20b8bf16f0ceb4e3ed85fb6278c2b033ddeebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull julia@sha256:08d617dd26dbd504f72d4b79f260ce56a70107e86c7511da1b7dac564e33cc06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2559029168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3451df9d4428574adb8c96a28dbf52fe5d2a476cd23c31f6a39e1cc1ddeb2a2e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:21:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:21:08 GMT
ENV JULIA_VERSION=1.11.5
# Fri, 18 Apr 2025 03:21:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Fri, 18 Apr 2025 03:21:09 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Fri, 18 Apr 2025 03:22:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:22:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6764394d4917248d1c1ab796596f1614518603a38026ddf5dd3d5755d24e3a99`  
		Last Modified: Fri, 18 Apr 2025 03:22:33 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e83ccc3d8eb956f1c55cf90c269deea2145ddc269932a8e0778175b5274ba60`  
		Last Modified: Fri, 18 Apr 2025 03:22:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442aa0c4a6f19e30b30923ea7691b2550bf0499525adebb9960b7d4d82ad6c04`  
		Last Modified: Fri, 18 Apr 2025 03:22:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b6ab8f5a0fb17a242af69276c59dc74bca90b6dbde4e0635db16970566e21`  
		Last Modified: Fri, 18 Apr 2025 03:22:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01579ce3c9bcf460fcc330733c8080e8dbb55e021abd9e6e066f05f0537492ce`  
		Last Modified: Fri, 18 Apr 2025 03:23:09 GMT  
		Size: 285.4 MB (285440134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe5863ab1bf23d62a04925ccdcf2930c2b26b93ff09050e42489540b40a48a3`  
		Last Modified: Fri, 18 Apr 2025 03:22:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
