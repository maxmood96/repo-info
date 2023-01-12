## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:d19e809fadfa5bbade49bb45c765ca0c46fa27e771285b521aa8ce461c4b4152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull mongo@sha256:fd99dffd4573a93a153efb7c848221b61e177a07329a18e7ac2ad0e431bce963
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1899310418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7600999929cdb4e9ab7933481492721b6665fbd78c242e8205a63574bb22b524`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 04:01:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 12 Jan 2023 04:01:10 GMT
ENV MONGO_VERSION=6.0.3
# Thu, 12 Jan 2023 04:01:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.3-signed.msi
# Thu, 12 Jan 2023 04:01:12 GMT
ENV MONGO_DOWNLOAD_SHA256=6557ae0360747d348aefdf30d1360f577804c446579c2012e0b04e5ec2489c49
# Thu, 12 Jan 2023 04:03:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 04:03:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Jan 2023 04:03:58 GMT
EXPOSE 27017
# Thu, 12 Jan 2023 04:03:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81c906622aa010adfaf1dd8c570ad750108a9b1a91ee1eb148e409e3e4fe68f`  
		Last Modified: Thu, 12 Jan 2023 04:37:06 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce95c72188062428a46e1f86fdc5bd368dde4322b63240048e9b2af047a2854`  
		Last Modified: Thu, 12 Jan 2023 04:37:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce7bbeb3cbe298cd1bb39cf45f798e1cf0322a72f24524b17884da07f8136c0`  
		Last Modified: Thu, 12 Jan 2023 04:37:06 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455b1f138a47c0146d292c2158bfe4d5b71381116bcc7510df017b2d6c530572`  
		Last Modified: Thu, 12 Jan 2023 04:37:04 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355ce8b8243b3d2c02b4b27c7bed07a419edb98949d09d3c8a6e6d6e578544e8`  
		Last Modified: Thu, 12 Jan 2023 04:38:47 GMT  
		Size: 513.3 MB (513271490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c3ae5918814d76132f4242714f9c7ddce5dfc3f4d5ae33fd99a514a692090`  
		Last Modified: Thu, 12 Jan 2023 04:37:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e690f8a040585f5c08a82d6906b9bda9b67a0641b98fa069fdae7f597875bb27`  
		Last Modified: Thu, 12 Jan 2023 04:37:04 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc3d106adc24f0c8a0923e770b6e0e89a658d26a179b3023386382ff490f2ed`  
		Last Modified: Thu, 12 Jan 2023 04:37:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull mongo@sha256:339c48347f6d5977d1ec349599a00d8fa1daacc363f8795ec3d9263192820572
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221016021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d3515f5aa5cb1bbb037a7062a214b8c80d1c3f304d6a46d9634f8e4be1a62e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 04:04:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 12 Jan 2023 04:04:13 GMT
ENV MONGO_VERSION=6.0.3
# Thu, 12 Jan 2023 04:04:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.3-signed.msi
# Thu, 12 Jan 2023 04:04:15 GMT
ENV MONGO_DOWNLOAD_SHA256=6557ae0360747d348aefdf30d1360f577804c446579c2012e0b04e5ec2489c49
# Thu, 12 Jan 2023 04:07:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 04:07:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Jan 2023 04:07:24 GMT
EXPOSE 27017
# Thu, 12 Jan 2023 04:07:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99eee4cf5f23d13a762e719b10916801f19f9df4bd7ff9b4c5cf57133b3dc04`  
		Last Modified: Thu, 12 Jan 2023 04:39:02 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a17b1e5f753f95e4025675034dc6fc1c34a55d73be80a8d50f79eb9e91a7cb4`  
		Last Modified: Thu, 12 Jan 2023 04:39:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60476112c06e5fe7639a2838ed0de7683814ff3f225f173e0369e0589e2d5dca`  
		Last Modified: Thu, 12 Jan 2023 04:39:02 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c5cee19e67fa5125be4ae14b2f98d626a3ddadba20999736a295890e20413d`  
		Last Modified: Thu, 12 Jan 2023 04:39:00 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68107f61d309beea8f31fff0fda8ddaae16083a2a93887eae9ee27424b2174`  
		Last Modified: Thu, 12 Jan 2023 04:40:42 GMT  
		Size: 513.1 MB (513062232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294d01bdf20843568daa51e19d2d286c74e655e4381ef593b33af2644062b2ab`  
		Last Modified: Thu, 12 Jan 2023 04:39:00 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f148c6bf2d553a41346396efac3d7ef1db13264383b29a7a62ccb17782b28e2a`  
		Last Modified: Thu, 12 Jan 2023 04:39:00 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c27b5e8dbb73924ddf83297d1f781b1d1130075828997faa00fa8dc446b827`  
		Last Modified: Thu, 12 Jan 2023 04:39:00 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
