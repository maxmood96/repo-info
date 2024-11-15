## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:1cbda4d8428750c7412fce944d3bc751410ba5378a1411a209d8fd45ebaf5aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull mongo@sha256:ba89f59c3f3e41795effd336da73356162b94317a2309fb079868629550d238a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565899482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62e8cf3667198127166f5865941e010713176c77bda058a86d450bde074cc83`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:09:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:09:14 GMT
ENV MONGO_VERSION=5.0.30
# Thu, 14 Nov 2024 20:09:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.30-signed.msi
# Thu, 14 Nov 2024 20:09:15 GMT
ENV MONGO_DOWNLOAD_SHA256=acabc07cba2e1b4a8bc2a852715a21ca29cae0f08a0dc157d54c1049f586fe45
# Thu, 14 Nov 2024 20:09:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:09:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:09:55 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:09:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13072491bd5927030e9c1ae0876eef777f3adf0e7c15e3464f80b9cae5425c69`  
		Last Modified: Thu, 14 Nov 2024 20:10:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b25e35e231e3b1cff4d777ff57e1830c47551a412c89d8d24926b171e37dcca`  
		Last Modified: Thu, 14 Nov 2024 20:10:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25699a395cdb133b518f09aa28ef9a83bdbd73094c10a22180ce871bf6fd76e0`  
		Last Modified: Thu, 14 Nov 2024 20:10:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e0245dafa663f004d8e7a94fcb761fce571cf3bebc68f2e9c3ef30ac189dff`  
		Last Modified: Thu, 14 Nov 2024 20:10:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2158bb947f7a2d23204c7454b99279902a56774a7228cf88a18d82d16a26d1c`  
		Last Modified: Thu, 14 Nov 2024 20:10:31 GMT  
		Size: 313.4 MB (313406257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823075f58f819e5a06dbbc5a55abf8a3798979c04ecd1f061ef97c2ecfd87322`  
		Last Modified: Thu, 14 Nov 2024 20:10:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a869e7901908dea09b4836ff65874a094d245d64639efc6c81fe994f32f4c6ca`  
		Last Modified: Thu, 14 Nov 2024 20:10:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc04efd6a909f97ee9a4717b19d36281b09a3f32cedd252dc5666fbc8442fa5`  
		Last Modified: Thu, 14 Nov 2024 20:10:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
