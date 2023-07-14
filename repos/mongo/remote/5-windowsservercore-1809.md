## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:63af2f5873183175ac025c126a15b7c581cd59a8447a251ed3eef3af0beaeb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull mongo@sha256:9a035ca48d59e90b7f183ad8109f405a450051398bf4a88272fb1a43b4948df0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2253756696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca70573d1b87adc56c74c58ff101bdd022d8cbc9a9880703b1ec6e93bae83170`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 04:20:35 GMT
ENV MONGO_VERSION=5.0.19
# Fri, 14 Jul 2023 04:20:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.19-signed.msi
# Fri, 14 Jul 2023 04:20:37 GMT
ENV MONGO_DOWNLOAD_SHA256=85c99b0b7ddeded924cb937d48fcd1b14c7c43b35c39fbd4d6961d6940f4b538
# Fri, 14 Jul 2023 04:22:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 14 Jul 2023 04:22:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:22:48 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:22:49 GMT
CMD ["mongod" "--bind_ip_all"]
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
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af7040112579bb5de51cd6e95a46de33aaf057c0eb7bdf2488c783d67554bc`  
		Last Modified: Fri, 14 Jul 2023 04:45:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6b3fdc20f03dd822afe4e9d9ced9dc44ee5764864eba4eab945512181bcea`  
		Last Modified: Fri, 14 Jul 2023 04:45:32 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b43b0c7ba1ad182a40d39b5e477a2ab1a06021deb97c73eff58c2d255208c`  
		Last Modified: Fri, 14 Jul 2023 04:45:30 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f77fb802a9f77d1a048a81aebec567a053f600e6d50976b02f7015bc9f0416`  
		Last Modified: Fri, 14 Jul 2023 04:46:33 GMT  
		Size: 314.1 MB (314057720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534b89020e3aa0832e3ce96056397abe4f2f2827fad3a8295df0b88d1cd94345`  
		Last Modified: Fri, 14 Jul 2023 04:45:30 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b805d54962a9d4c15cd521bb9f51124f73bc7a514a29af5e68226a5ef8ea8f`  
		Last Modified: Fri, 14 Jul 2023 04:45:30 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2d4d558465653596ffeb56f638af654af75a36fac66a57869062a6c7336d5`  
		Last Modified: Fri, 14 Jul 2023 04:45:30 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
