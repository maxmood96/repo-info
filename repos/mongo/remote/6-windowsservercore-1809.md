## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:00457837bde1d6de5c3bad886555ede8efad29788b436a615d3c257d98888cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:76e8387e2b303d4cd4778ebecb6725cb835138a61ec5e8a58f838f1069d6d5cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769479240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5c37111a6e4ca75f2eec26066a60f4a62721730bc899644b71eb702c52a225`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:23:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:23:54 GMT
ENV MONGO_VERSION=6.0.16
# Tue, 13 Aug 2024 20:23:54 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.16-signed.msi
# Tue, 13 Aug 2024 20:23:55 GMT
ENV MONGO_DOWNLOAD_SHA256=4a0da9d2a8e7151a2c7c8e68406dce00336f2bb2f6b9f1129184c9888c59e032
# Tue, 13 Aug 2024 20:25:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:25:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:25:52 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:25:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e157576b3448ceef2ace69241a236a06e8ac20270311b5eaca2ea60cc32879d1`  
		Last Modified: Tue, 13 Aug 2024 20:25:56 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534de3a26ecb33bebfc1e435c045bfcde9094a71b2bb06389d638957950470d9`  
		Last Modified: Tue, 13 Aug 2024 20:25:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb03c7a173c2371b9d72458c5cc0df82bf272e9830a9293022bc9394a0cfae3`  
		Last Modified: Tue, 13 Aug 2024 20:25:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde6c1cb09478672155482006428d7eb13cfd863840fd7adf3f8ab5b0e8a8d8e`  
		Last Modified: Tue, 13 Aug 2024 20:25:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e93be56fc87f23982cfe52d7f2fa0e5c12380717880eac74325f4c93493880`  
		Last Modified: Tue, 13 Aug 2024 20:26:39 GMT  
		Size: 524.3 MB (524266933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6719df67e94afb3ab87f2a207ab206e78de3321c84ad4d5447c2fda2b51785ca`  
		Last Modified: Tue, 13 Aug 2024 20:25:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73995ddda7699e4b5ccc690bb29acfb5a98dfa335fd201614400f7c4cfa90059`  
		Last Modified: Tue, 13 Aug 2024 20:25:55 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f2b8d8fc95821a122f0f2ddf0eb452fa0a79cf868a3261c842f5114261feee`  
		Last Modified: Tue, 13 Aug 2024 20:25:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
