## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:38978e4dc66c74f478ca62dea71d0ac42e19dfb9d4fad834e6db395dbb9d059c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.1850; amd64

```console
$ docker pull julia@sha256:9fd3121ded0bca6aae979bcda27759154cd3fdf2a289911e25c4dec58aaf0b9d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1898933811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c349f74f061dbd6b8085e4ff0a73406028036c76f42858a2cd1e2ee68ac6343`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 02:56:24 GMT
ENV JULIA_VERSION=1.9.2
# Fri, 14 Jul 2023 02:56:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.2-win64.exe
# Fri, 14 Jul 2023 02:56:25 GMT
ENV JULIA_SHA256=bcc8a0eb217ee128638e12b756e1f41df5c83cff6c6749839d081618f6c79e57
# Fri, 14 Jul 2023 02:57:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 14 Jul 2023 02:57:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3868afb870cbd85429761170a65b049ab18d8d104a9ad31433a3267e0ada75d3`  
		Last Modified: Fri, 14 Jul 2023 03:06:53 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91d4adcf24935bbc65c49a4775d25c72452d06ee312d1d81b675a2154dcdaa7`  
		Last Modified: Fri, 14 Jul 2023 03:06:53 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2249be739f084c57b7668fe0a401d6bfa489fd381ab1aaaa3028fd60f38875`  
		Last Modified: Fri, 14 Jul 2023 03:06:53 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169261f12f2f717b0dc22927f8e63fccf230fb557b42327ce232598fd8d2559b`  
		Last Modified: Fri, 14 Jul 2023 03:07:29 GMT  
		Size: 161.6 MB (161561517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c0fe26a80bb62ad03c664a4887d753eaffe780bdc84e4606dffe45e30f44d6`  
		Last Modified: Fri, 14 Jul 2023 03:06:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull julia@sha256:ab90502294b6eb3bcf0fba3b83ee6ffbef8e85baf167539f4970f1b73d85d633
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2101255703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512b64d0db616788a44721d4274a3718a85e49f1c78e2623ec45d24c367e4be1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 02:58:07 GMT
ENV JULIA_VERSION=1.9.2
# Fri, 14 Jul 2023 02:58:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.2-win64.exe
# Fri, 14 Jul 2023 02:58:08 GMT
ENV JULIA_SHA256=bcc8a0eb217ee128638e12b756e1f41df5c83cff6c6749839d081618f6c79e57
# Fri, 14 Jul 2023 03:00:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 14 Jul 2023 03:00:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c918aa23fe95aa26b065a54e59bec34d88c9a1668beec130ce2784e2b16707c7`  
		Last Modified: Fri, 14 Jul 2023 03:07:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e4e459afb23afe9ac3348432d573d91f4a8fe5cbfb6197dfb8eb3e724d348`  
		Last Modified: Fri, 14 Jul 2023 03:07:43 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d24cccdab5d5d797c0ed95268654ddc58151cedd451459ae9ea6cf17ea0a3`  
		Last Modified: Fri, 14 Jul 2023 03:07:43 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610e4a62f061ea84f63cbb15107a683e8e90f80bdc07db1be896d9336359bef`  
		Last Modified: Fri, 14 Jul 2023 03:08:19 GMT  
		Size: 161.6 MB (161559634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4038516eeab65f56d031215bead5ab4b81fd0e748ebb1434617b08ab8a7e73`  
		Last Modified: Fri, 14 Jul 2023 03:07:43 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
