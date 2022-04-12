## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:72b958ebeff3ace4f84f53b7aba616a13f4e49c5ef33335fc0c1049091d6b7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull mongo@sha256:44ad7b8c9edbce010b418d33261411ebc10675064cbe0fc25717874cd657709b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528153248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a37120d1d3f6b04302904b41039221282c2cd92840549446c7f3d6ae8af347`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 20:08:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 11 Apr 2022 21:14:41 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:14:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.7-signed.msi
# Mon, 11 Apr 2022 21:14:43 GMT
ENV MONGO_DOWNLOAD_SHA256=3d9eee63d56ff75176cf03308274a29c9e385704e21a26f5864cfe1357ca3cf7
# Mon, 11 Apr 2022 21:16:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 11 Apr 2022 21:16:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 11 Apr 2022 21:16:20 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:16:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:100676d020cbb3f3df522078bdbd67f9bbdab3dee71a4ec647a43b6b2b1e0b8f`  
		Last Modified: Tue, 08 Mar 2022 20:37:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92292e14b93ac6731aced73f893f48c7685007cde53bae6beabc8ca3ceda47ef`  
		Last Modified: Mon, 11 Apr 2022 21:23:50 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a2ad89a7aecda4d264d8d848f9fe355cd7e60915b4f54902a5f936499ef2bc`  
		Last Modified: Mon, 11 Apr 2022 21:23:50 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a076b56a1d4e097beb6bd5e373ffee4b39681955bc2cc099884c8ab1e95b2b`  
		Last Modified: Mon, 11 Apr 2022 21:23:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b8b937642be78da649eca87ac886dcbb95a8053f76c4531ad1036a8ef3ebbd`  
		Last Modified: Mon, 11 Apr 2022 21:24:43 GMT  
		Size: 306.9 MB (306896479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ebc1ab65fd0ef04669a84cd7103585ba0876684b090332e499d36c31897b88`  
		Last Modified: Mon, 11 Apr 2022 21:23:48 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f898ef7a67afcea2ccee354d2993f572f99d49b17f023b12786ba33c225c69da`  
		Last Modified: Mon, 11 Apr 2022 21:23:48 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eccec6966ef496aefaec0ea2d9736899e277e647e04987f6264bc60e17b7dc4`  
		Last Modified: Mon, 11 Apr 2022 21:23:48 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull mongo@sha256:03f858171ac6b7ed0b5784201ff189d972ab5b5e0b97dd96ed87bf72753ea64f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3022164932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984ad89a643b50a9d3e2296aa0308f3c26e56f183b5dcb9d5c5acec45fb7e632`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 11 Apr 2022 21:16:38 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:16:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.7-signed.msi
# Mon, 11 Apr 2022 21:16:40 GMT
ENV MONGO_DOWNLOAD_SHA256=3d9eee63d56ff75176cf03308274a29c9e385704e21a26f5864cfe1357ca3cf7
# Mon, 11 Apr 2022 21:19:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 11 Apr 2022 21:19:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 11 Apr 2022 21:19:11 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:19:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b5610ee4b97b080045e93d88fd248bb42fd950969ea046c4f003f718ae4e1`  
		Last Modified: Mon, 11 Apr 2022 21:25:01 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fd1e97dbdd05337518d4ddb8177562c10bbb5f17d6fe7f5b06bfeaaaff8d62`  
		Last Modified: Mon, 11 Apr 2022 21:25:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d40847059bebca2ab2ae641d40230bdab5893bab72b94ceb3593e90443202a`  
		Last Modified: Mon, 11 Apr 2022 21:24:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade61cb302931b22d348fe635139e26fb1eec4aef7988c76252e6bd6b065b8e8`  
		Last Modified: Mon, 11 Apr 2022 21:25:53 GMT  
		Size: 306.7 MB (306702364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a19078cf9c9891ba54b39168db873a9cd71aba2bac667a2b8a451d9ddf17529`  
		Last Modified: Mon, 11 Apr 2022 21:24:59 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1cb85525901728c4b5f3633e8265f3cd5392a09f79e729979fb7c83c406178`  
		Last Modified: Mon, 11 Apr 2022 21:24:59 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df45aa1a6375bc40bbe50e0b0cc4b1e4d0deaeae67918d75d9dd3c011e29f82`  
		Last Modified: Mon, 11 Apr 2022 21:24:59 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
