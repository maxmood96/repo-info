## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:aa5669cddba9771739a5228c525963438e5b26e4ccaae858f88ee78056d3ff78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull mongo@sha256:170c20dd31da2ca1500fa43a2a74b35e69622969707f6c715907b3a1694190cb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311327496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17c13fe5ec3fd6ae1d8af677bf51c2e760ff334440ca5712d2e12a56bdec7c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 10 Feb 2026 20:08:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 20:08:02 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 20:08:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 20:08:04 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 20:11:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 20:11:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 20:11:02 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 20:11:03 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a5aa8e1fa5bfac31a0104db90a5921227d523903954a1cec1b0751def99fb5`  
		Last Modified: Tue, 10 Feb 2026 20:11:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69163faf7e48c29688b0944c7e1f746e5f0058a9289a07017244d2cd9cca3f80`  
		Last Modified: Tue, 10 Feb 2026 20:11:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db06eaf9c846c38f7978021dbde25c2a0ed233878f460c05200c90a4c2698c69`  
		Last Modified: Tue, 10 Feb 2026 20:11:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1079daf0f10af02ebd51b79285e91a703ab781503a58ee458645b5c7b127652c`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f82d7a8018f15862f50ea18d814e4133c36986c0f103437fc23031fe7201`  
		Last Modified: Tue, 10 Feb 2026 20:12:19 GMT  
		Size: 815.6 MB (815558023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404b04dce76f2cc2f2a0eb01976bde1cee8b0c123638067551788ebdf334dafb`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f89c6f82137af6cf42b3ffdc7b7929246605574f5afa22ea57fd5f03d9d1f`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7bfa7240b3acb6d1e1ce50e1136075cd480c5fba0f01d64ab9cfd27200e02c`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:89cddea5e092492bee49228fd4b0f7f373265aae475acb419347dfad1695f483
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651329165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f23c3e1dc86bab94a343e4424e16fdaea2f1a8f4254fed36127f6e26687dc5a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 10 Feb 2026 20:07:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 20:07:36 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 20:07:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 20:07:39 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 20:16:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 20:16:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 20:16:35 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 20:16:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbb8634e74e491bdc6a22032c284cc3c0c84bab70419b7d7d14957a4ab7e07`  
		Last Modified: Tue, 10 Feb 2026 20:16:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010a9cf5397cfc1f05504fc9e97106fa2239f54d8d2c172ae640aa5cb9d054e9`  
		Last Modified: Tue, 10 Feb 2026 20:16:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256a9f793f11909aba07f4884482025a9eab17860c836795c797e2b154a1865f`  
		Last Modified: Tue, 10 Feb 2026 20:16:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56a8d3f6cf37062f6fd0bfa87044b60e70d459934be9d878a1d751c3d31e5e5`  
		Last Modified: Tue, 10 Feb 2026 20:16:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f235f5a55b18a5ffe472281b58a5b028b9b5b97b271d90f061fcec2cfc8e477b`  
		Last Modified: Tue, 10 Feb 2026 20:18:02 GMT  
		Size: 815.7 MB (815660824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01b97439d89ebdcd2ea54ebf48842b2357b14f30865a2fde527fae036af6474`  
		Last Modified: Tue, 10 Feb 2026 20:16:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a3223389a6fad7b27de9f7e135f38415de5c97eb80e161f51ef20cf8936518`  
		Last Modified: Tue, 10 Feb 2026 20:16:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d13dbd40418a8d7a53562f609b093f9d72a2a62414ca8f43ed5baa968e8b0e`  
		Last Modified: Tue, 10 Feb 2026 20:16:50 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
