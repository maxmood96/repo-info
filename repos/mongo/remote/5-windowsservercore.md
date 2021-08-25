## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:bc4bbeb3ae7ea961f7f06cccea3d0af185f22e26c2324c7ce60bef4807a39ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `mongo:5-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull mongo@sha256:d1592975df2f53e365352c4655ff95543776f3f87803222a1ae4eca3f9fcd4b0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2976772404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881b0b5e414a3c1a9d294850aa2e841cb216d9f9905ebbf008cb326abd8672c6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 25 Aug 2021 13:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 19:38:11 GMT
ENV MONGO_VERSION=5.0.2
# Wed, 25 Aug 2021 19:38:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.2-signed.msi
# Wed, 25 Aug 2021 19:38:13 GMT
ENV MONGO_DOWNLOAD_SHA256=8c517e4b1598d627ee16c2dd45be90397bf040cf2845eef2aff0b9bc25062228
# Wed, 25 Aug 2021 19:40:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 19:40:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 25 Aug 2021 19:40:15 GMT
EXPOSE 27017
# Wed, 25 Aug 2021 19:40:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:985da5cbc0735e1c422e766af23125ba345f431cb337ea43ec32298d0bb8e4ea`  
		Last Modified: Wed, 25 Aug 2021 15:45:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658daa6e465de2e8f951f7cc7f7fc7bcac7946ca1d3a281ab8080f828ed47a95`  
		Last Modified: Wed, 25 Aug 2021 20:01:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53b88d0d8031cad96cddf85893e17fbcf1f81c7ecc57e35d89e5139f1a9f399`  
		Last Modified: Wed, 25 Aug 2021 20:01:57 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf20037e536db8e6ecf6ca661157a1a13428891172fec3b39e1b58a50a1146`  
		Last Modified: Wed, 25 Aug 2021 20:01:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1227c86fa7a71ea32cd31b6f7623bf109919d7be73af22a4bca0c302cfbe83d0`  
		Last Modified: Wed, 25 Aug 2021 20:02:45 GMT  
		Size: 290.8 MB (290765245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbc30f10f98aa8cfb33527e195657371709483ca7f3ac3823f37ba6633dd971`  
		Last Modified: Wed, 25 Aug 2021 20:01:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df248022067962cd2e97a4f5830c039784df486f4470d5479bcf74cb2b98f521`  
		Last Modified: Wed, 25 Aug 2021 20:01:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a2e173c76c2274f766c62c19c9459c263d9ca1e817fd332a4d2ceb096c96de`  
		Last Modified: Wed, 25 Aug 2021 20:01:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull mongo@sha256:28fc771fc3e4cf094c86ef62e719a879cfa6ce994d84d212f23c3c69b8af9469
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6566098677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac1ce88c047426be2b4ee87af431bd3ac3185dcae6b12f9cf2a57c3d7e9dc6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 19:40:23 GMT
ENV MONGO_VERSION=5.0.2
# Wed, 25 Aug 2021 19:40:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.2-signed.msi
# Wed, 25 Aug 2021 19:40:24 GMT
ENV MONGO_DOWNLOAD_SHA256=8c517e4b1598d627ee16c2dd45be90397bf040cf2845eef2aff0b9bc25062228
# Wed, 25 Aug 2021 19:42:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 19:42:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 25 Aug 2021 19:42:40 GMT
EXPOSE 27017
# Wed, 25 Aug 2021 19:42:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a869803fc3d8292f0fe1bc6ed35e1ceedbd7c797a1486767a55f88c6c28ed4c5`  
		Last Modified: Wed, 25 Aug 2021 15:45:25 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae64dd51cae865b4fb1f2dff46a2a28c142afc717d2bf51d33fa91044f3b89c`  
		Last Modified: Wed, 25 Aug 2021 20:03:03 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9fdae42abe869550529825a5ed22a28d10d7b723d1b1c36dd70a3c66f2087`  
		Last Modified: Wed, 25 Aug 2021 20:03:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11515d204e6c2d6b6ee5e319faca359304331db62af63ee66ee79110920df48a`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96873d298adf1b77548a67c52c60bf53094d7152fedab2839da13ee2353c9c74`  
		Last Modified: Wed, 25 Aug 2021 20:03:52 GMT  
		Size: 295.1 MB (295123000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd183858c1b7762db7816f865b42952b23b8842785235492250805c2b1bf15a`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9969cdae0a3da21fd9c98332f01a059a52048731d43587716a9c52b41a5eaff`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a58437c09d52d08db591ccbcc6a9fda4772573cbf4dafc72f943c01061d9d`  
		Last Modified: Wed, 25 Aug 2021 20:03:00 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
