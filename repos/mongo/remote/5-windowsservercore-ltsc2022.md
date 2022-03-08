## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:3b08b9ad66cccb821d95460d1a667fe93b1f638e4116162690029d213afe26d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull mongo@sha256:565f4503fdf40e345bd6971dc8e55fa652e1e12dc3665d0bc640e1b9aac31d0e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2524935667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676bddbcc54562d04f62a3b5a184d6e167327e405528d01fea1ce6d84b073c6a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 20:08:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 08 Mar 2022 20:08:18 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 08 Mar 2022 20:08:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.6-signed.msi
# Tue, 08 Mar 2022 20:08:20 GMT
ENV MONGO_DOWNLOAD_SHA256=f6e2bc600b2b8b0251a9e99d84fefc43c66e45deb5793ed8e65cd12a318c76ee
# Tue, 08 Mar 2022 20:09:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 08 Mar 2022 20:09:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:09:49 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:09:50 GMT
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
	-	`sha256:92c9d2089e83e0db436c1ab530847faf62ff24e52888f6fba1aeaeb3137137bf`  
		Last Modified: Tue, 08 Mar 2022 20:37:10 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9f4d1cc4ade3ac05844200b4d2054f337b5961eae3dca978b65e2c7d2eaa5`  
		Last Modified: Tue, 08 Mar 2022 20:37:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a05a9f46d9482a199122a3a7b0f82dfa9dae53f6f208fc2477b7cb9c7fd9e7`  
		Last Modified: Tue, 08 Mar 2022 20:37:08 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16afd9689041bd078641ba29b412011757a6228323b4af23eb1b0777896b5825`  
		Last Modified: Tue, 08 Mar 2022 20:38:05 GMT  
		Size: 303.7 MB (303679286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91541010666fad983e005f73c8e99c215604519ea8350d628b9b067ffd6dc65`  
		Last Modified: Tue, 08 Mar 2022 20:37:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a847cb9135213cda2ebb56df53c93fbf240309f67a41ba766d47efee72085e`  
		Last Modified: Tue, 08 Mar 2022 20:37:08 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160777a0193ce1d56a06deeaaa612777de792729b467b69ff640aabab35a806d`  
		Last Modified: Tue, 08 Mar 2022 20:37:08 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
