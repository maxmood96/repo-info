## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:86dbbf011fec64d98de0c8f9b86f646b14862ec2bedc122a52d8b5ee064e2f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:0047939eff88b782c65c9535452678a8ea0e63db144bd90982bcaf9c8ab4a8c1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2168391687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d58d25a9023ba92442327d669850413fcd4fdb4b5b82b4408ebeb9124a269c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 02:28:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 30 Jun 2023 23:32:17 GMT
ENV MONGO_VERSION=6.0.7
# Fri, 30 Jun 2023 23:32:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.7-signed.msi
# Fri, 30 Jun 2023 23:32:19 GMT
ENV MONGO_DOWNLOAD_SHA256=41dabd0f59813c675f6973201374800b300800060839968b9fda7371423061b1
# Fri, 30 Jun 2023 23:34:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 30 Jun 2023 23:34:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 30 Jun 2023 23:34:20 GMT
EXPOSE 27017
# Fri, 30 Jun 2023 23:34:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9634b679e6c602a6aaf0bae51625e7ca041489c77150db557640304f51bb37`  
		Last Modified: Sat, 24 Jun 2023 03:01:43 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a307fac960c5ab587a74c6a52793636337c1fb8be19a1606b125e60abfbd17c`  
		Last Modified: Sat, 01 Jul 2023 00:33:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0853bd64323c5c83fb0cd3ffa295c5c2c04ce4d067916f3a4e03522c2023f3`  
		Last Modified: Sat, 01 Jul 2023 00:33:07 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd92a34f4fe0ef067dd91ca0f2fed7bc3f71aff01f194c968015743318c18787`  
		Last Modified: Sat, 01 Jul 2023 00:33:05 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146e83a613bd06812fd98bb7bfc0681f082481dd8be04495f71f99ebb5a6e888`  
		Last Modified: Sat, 01 Jul 2023 00:34:19 GMT  
		Size: 517.6 MB (517645190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92437d4c9785f7a5b9a89d3b174596de346aef1fbdc7b8d10875ea79fb279a2f`  
		Last Modified: Sat, 01 Jul 2023 00:33:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83149c6e4f5aee6cf435ab3ee11f2485e23732d6b29ef638065de814a04e634f`  
		Last Modified: Sat, 01 Jul 2023 00:33:05 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0d320ea910bea1472ae3d2fb7c1a0de8240409efcf5ff7c1ce4fac269e91e3`  
		Last Modified: Sat, 01 Jul 2023 00:33:05 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
