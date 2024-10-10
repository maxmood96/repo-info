## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d52c93e4cb9d9fbbf19e93b88f3e346de5e8091615ee5511ea848cf297714687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:73ee37717ffe1f284d4d98822d778ee6f6c9d53862fde54f29f0e255bafa8a37
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052192330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9515b762bde6ef52a8e4f3dbec095f0b9ae0029c15dc813ef018f2ed7557e28a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:09:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:09:20 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 23:09:21 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 23:09:22 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 23:10:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:10:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151c8a852f1434413dbef062d9c7d2c6be7fc62aa723a4e52f376286735f8688`  
		Last Modified: Wed, 09 Oct 2024 23:10:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177a6978bfc7a9160b1da6330fe662dbbba408bf229e7a22bfd14a2b8d856e10`  
		Last Modified: Wed, 09 Oct 2024 23:10:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28dbfa238f8c3555c58e4f05d23a362b64921e3cef6825cd81db7566935967`  
		Last Modified: Wed, 09 Oct 2024 23:10:50 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ea11c36b329f922876008f5b54ad297f74437d7406014adfdc7443b96143ac`  
		Last Modified: Wed, 09 Oct 2024 23:10:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bcf28d73519cf1657bf0e053a571fd497e3f2914e720425fc64ba9438d4c79`  
		Last Modified: Wed, 09 Oct 2024 23:11:24 GMT  
		Size: 252.8 MB (252844374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455cedd7059c05a656cd6e0e8ba2fa01f10bfbab766e480e165bacd57d080a54`  
		Last Modified: Wed, 09 Oct 2024 23:10:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
