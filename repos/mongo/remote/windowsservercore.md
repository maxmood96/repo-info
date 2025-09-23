## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:f7e7b23c2c56ba9e9fd03dfc3e04a422c214cd5c7a531dea975911841ba97e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull mongo@sha256:0de701cce332bf7c3b409d91cf2b725c8604c9294ffd00f6329727962105a053
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 GB (4355957720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf6e0eec82f1f3c7d8fbafa150222e7db2c0a2f5d57e7473aef1e361629012`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 22 Sep 2025 22:12:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 22 Sep 2025 22:12:17 GMT
ENV MONGO_VERSION=8.0.14
# Mon, 22 Sep 2025 22:12:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.14-signed.msi
# Mon, 22 Sep 2025 22:12:20 GMT
ENV MONGO_DOWNLOAD_SHA256=9374f9eb0449d1099b31d89376ae47ba5e088ba7a9b0f5a9155435c8bc6567bb
# Mon, 22 Sep 2025 22:15:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 22 Sep 2025 22:15:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 22 Sep 2025 22:15:48 GMT
EXPOSE 27017
# Mon, 22 Sep 2025 22:15:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d909f29012e278681ca09ca8bc87b25b47194905028a6c91f9ca3ef9c3a29656`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ce938b921e2484a8ee2187e346f18aee6cda5b61d49ee75919ddc379285b06`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18da0914d9f735e93ac8b4292cd1b13555974d5b0cb5e4597ccbe74598581a`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4693a46c03767709eed5e7e023dc872254aeba67c85b956f3eb64179d22ac0`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8988c7f1f7ab2da2479ba65c002d5ead4d7b999e29630885b107b8dac65c90a`  
		Last Modified: Tue, 23 Sep 2025 01:08:50 GMT  
		Size: 784.5 MB (784508802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309071b742d3cc81433635fe6b33529f1f62830587d438c8067ecc8ebacb3be`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f26d3f6ce50828a4beb906d996ecbe802534a9106c13ee8d3010745ded6a1c6`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83912d64c2763a0eadf80777528a3841ba4ef988e77a4ad2d24a167f9f9af2c`  
		Last Modified: Mon, 22 Sep 2025 22:30:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull mongo@sha256:3b2716d3b20039834317b3ba2af1634fbb31030178705f293907a67b1cea9b06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3066595888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134cc1e4b94c0e1dd22c41f90e23ca2a34e836f696a15fe127723ab567fb9e85`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Mon, 22 Sep 2025 22:11:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 22 Sep 2025 22:11:06 GMT
ENV MONGO_VERSION=8.0.14
# Mon, 22 Sep 2025 22:11:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.14-signed.msi
# Mon, 22 Sep 2025 22:11:07 GMT
ENV MONGO_DOWNLOAD_SHA256=9374f9eb0449d1099b31d89376ae47ba5e088ba7a9b0f5a9155435c8bc6567bb
# Mon, 22 Sep 2025 22:19:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 22 Sep 2025 22:19:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 22 Sep 2025 22:19:21 GMT
EXPOSE 27017
# Mon, 22 Sep 2025 22:19:22 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:e89a4021f8dc5fa397787c8c655f52bf5cf772acc20291d6286769158d5f83b9`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b49840f8d9036c19e77e8434120e0338f532e38fc45265953846f20fd8922e`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4ea5d94dc94bf92d43fe8953bedf8829431c223f4a434d2d57fa5d555c50e5`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f73042271b3c7be7e2788969b8f68a78f0e2d8c429b2297aa881f665f8ff21`  
		Last Modified: Mon, 22 Sep 2025 22:20:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2bce694a973b9260face23883989156975dc4c629a489fcdcce2865338f71b`  
		Last Modified: Mon, 22 Sep 2025 23:11:54 GMT  
		Size: 784.4 MB (784441725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e441b680d7ac73c0d11b31cf8128033a2c9d4621b8221c8ec06ed16228a7fa`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8c1f111134326750e8c74806ff90ffe8096ad57bbca8f462092353aa60f66c`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42ef08ca9bf87eb1dd2990fdc8645bedc2a95a366d92901dbb87a70ab88a0a9`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
