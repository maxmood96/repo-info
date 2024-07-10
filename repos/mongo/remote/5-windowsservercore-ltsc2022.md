## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:be7a2e7b9dc3bf429bbb763a52be24252d3211fc7a4ae6b7c5162ec81fe68619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull mongo@sha256:76f6971b432cfeb49d48f7ea37601b903e45234d9af05fe05817abf2cc221945
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452127570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81afb0454496712528c4f6c3bc41f4ba4aeaac1934dbce4e75ca8202312d9810`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:04:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:04:54 GMT
ENV MONGO_VERSION=5.0.27
# Wed, 10 Jul 2024 17:04:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.27-signed.msi
# Wed, 10 Jul 2024 17:04:56 GMT
ENV MONGO_DOWNLOAD_SHA256=3da3dc8c13ddb8405c230c8495d4412d9a847b6c24e937b63c6b67437984a175
# Wed, 10 Jul 2024 17:05:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:05:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jul 2024 17:05:49 GMT
EXPOSE 27017
# Wed, 10 Jul 2024 17:05:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89452dfe7a6e5ba17998f6b25a3f826d7d02a975ff9bd993128283f149b514b`  
		Last Modified: Wed, 10 Jul 2024 17:05:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c088c55fcd936ddb18b54acccc9f98ea6cba9a756ba00e7a50c4f6ac5d487967`  
		Last Modified: Wed, 10 Jul 2024 17:05:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b2fd218d00147d32591bbaac522b4139ecc6603799688be32b11acaf7ac04b`  
		Last Modified: Wed, 10 Jul 2024 17:05:55 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb86097034e9040b32844a61c781de01beb8fe43c692a941b827c2557b17710`  
		Last Modified: Wed, 10 Jul 2024 17:05:53 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407ef8b1741325d4acdf5877324a50e52ee468374833c1b2c96ac79ef01e3730`  
		Last Modified: Wed, 10 Jul 2024 17:06:24 GMT  
		Size: 312.5 MB (312518207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707eab8f339ca74ca29a545716d8fc9cfb5fd96c76293a50be72801f013bdd8a`  
		Last Modified: Wed, 10 Jul 2024 17:05:53 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12c89ee0a8d43b714a28f959a52c36563e7497e0aaa97bf8b9ccad83e12dd91`  
		Last Modified: Wed, 10 Jul 2024 17:05:53 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcc152eceb2a43628175fc18b1dee586ae340af01c9a3288c6fe70da12f9655`  
		Last Modified: Wed, 10 Jul 2024 17:05:53 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
