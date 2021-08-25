## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:a9175549b1110dfc8a4d2219ca34d078c3a82c5fe191a38cb1c085002e06358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `mongo:4-windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull mongo@sha256:912855ae9aa39086cbe2daa950daf4e331ea9b8e3e4774cc861b5749d1caeade
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2918164481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfae59b70304e52411add293724ef420cf580e1259237a0903d9c20e881c649`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 25 Aug 2021 13:46:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 19:44:00 GMT
ENV MONGO_VERSION=4.4.8
# Wed, 25 Aug 2021 19:44:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.8-signed.msi
# Wed, 25 Aug 2021 19:44:02 GMT
ENV MONGO_DOWNLOAD_SHA256=b66e3beafa5623eced86f0a7298932918ccd27199e572021f7e8ea074cc51f23
# Wed, 25 Aug 2021 19:46:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 19:46:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 25 Aug 2021 19:46:05 GMT
EXPOSE 27017
# Wed, 25 Aug 2021 19:46:06 GMT
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
	-	`sha256:e800f1be05173099b95b65cc65a911e5f87277499d433ce110b3357b7cefeecb`  
		Last Modified: Wed, 25 Aug 2021 20:09:28 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643130984c97afea7f50714297b174a6030886462f11bab20d85c4e84ef833bb`  
		Last Modified: Wed, 25 Aug 2021 20:09:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617046b010d3c7ef816cbeeb4952e6874a5db0fbc013966bc1bf637303a9c09f`  
		Last Modified: Wed, 25 Aug 2021 20:09:27 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbb784d9bd78e726ada105ec93a56ad363353633669fe14a56155f687cb619b`  
		Last Modified: Wed, 25 Aug 2021 20:13:25 GMT  
		Size: 232.2 MB (232156736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88f37facca495a06437114a1b26f6b6efa23fd6b5e71136ad783f4426e7693f`  
		Last Modified: Wed, 25 Aug 2021 20:09:26 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628047f17808229c3e9bdf13661541947a3f8a22d93b9d6b517ec7b380cb68c`  
		Last Modified: Wed, 25 Aug 2021 20:09:26 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0403565a4718fc22e8f49f9fdfa4cb2221dce586811b35c6b93720c67b55e0ee`  
		Last Modified: Wed, 25 Aug 2021 20:09:26 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull mongo@sha256:7fdf2fc8066dbe5e79f127a53b9638880d52de17651fcabac3ea30552f2d35a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6503038724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7566104a909a7536f6fc50239248d423ed29cdf293eb3666919a3f4c67e18dd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 25 Aug 2021 13:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 25 Aug 2021 19:46:25 GMT
ENV MONGO_VERSION=4.4.8
# Wed, 25 Aug 2021 19:46:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.8-signed.msi
# Wed, 25 Aug 2021 19:46:27 GMT
ENV MONGO_DOWNLOAD_SHA256=b66e3beafa5623eced86f0a7298932918ccd27199e572021f7e8ea074cc51f23
# Wed, 25 Aug 2021 19:48:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 25 Aug 2021 19:48:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 25 Aug 2021 19:48:25 GMT
EXPOSE 27017
# Wed, 25 Aug 2021 19:48:27 GMT
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
	-	`sha256:f3ff95960d38c472b8bf8a474cacf72c4e454c76fcb3a7918f501cc8f7711bfd`  
		Last Modified: Wed, 25 Aug 2021 20:13:42 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ad601ceee4603a71ea1c945cef419e8d84f4f15d27f72f328c01a870eae8e4`  
		Last Modified: Wed, 25 Aug 2021 20:13:42 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10580b73f6c3050bef19dc30210068b87b999276f6a854192de5112ce791307a`  
		Last Modified: Wed, 25 Aug 2021 20:13:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b34ff72c76ec07e10d212e47bc32845efe3fa403a26fb93c9cf465866cc4f9`  
		Last Modified: Wed, 25 Aug 2021 20:17:42 GMT  
		Size: 232.1 MB (232062756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db3a9984169c9689749e70a303523df47ef67af1e6d97d89a9fbf16a7b28dee`  
		Last Modified: Wed, 25 Aug 2021 20:13:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5a5e4e2bb9f9ceea38460527c29cab909428dfcd4956c3b2c2cd6988d71d2e`  
		Last Modified: Wed, 25 Aug 2021 20:13:40 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91ca0de555db29ea1c02d115bb60b8186e02c247517d49cf58e6f4de412a98e`  
		Last Modified: Wed, 25 Aug 2021 20:13:39 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
