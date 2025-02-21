## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
