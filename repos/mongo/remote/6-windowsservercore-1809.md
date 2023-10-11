## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:fe5d0975d4942c0f07f1e82251af68f0d69c494acec8f88abd0ff38b531f1ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:a6b270930494084f340e52ef2fb9f07057ea048649923eacf17ea84ccf33485f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548811101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75455d71657231573f55a2a13f6212c0aace6d702dfec7f19de884c7b9c8b741`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:11:45 GMT
ENV MONGO_VERSION=6.0.10
# Wed, 11 Oct 2023 03:11:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.10-signed.msi
# Wed, 11 Oct 2023 03:11:47 GMT
ENV MONGO_DOWNLOAD_SHA256=11892a8a8eda913e7146ac547885f2ed637a1ec3b74bfb7c8d26a11ef6a4ac9c
# Wed, 11 Oct 2023 03:15:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 03:15:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 03:15:37 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 03:15:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d4088acdd972e10cf2c26dbe5b91d30300a9b3e568976a881707c40f946246`  
		Last Modified: Wed, 11 Oct 2023 07:45:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155a9242ca95ae32f7eebca2a8f63eed71c896f648aa949d51f32879841d935d`  
		Last Modified: Wed, 11 Oct 2023 07:45:53 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a3b10a0b23427f497087942f02f967d89c9b8712c06794dc377b6607da0dc1`  
		Last Modified: Wed, 11 Oct 2023 07:45:51 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5c097db9a2daddcb97debcf2e316414b105badbe131bdbb5d946fe17a4afee`  
		Last Modified: Wed, 11 Oct 2023 07:46:59 GMT  
		Size: 517.2 MB (517211032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7f7e75442fda7dcaad41942143a9569102e4005550dfbf50b6c51a8c66be27`  
		Last Modified: Wed, 11 Oct 2023 07:45:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaf8a9e92786495433b0b43fbadc2183557e86bdd62e13edf0bc905998c82d`  
		Last Modified: Wed, 11 Oct 2023 07:45:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e99442aa759eb14db2e69f8005a6bf7bd269c26fd8afa02e8dba85c4f552f8`  
		Last Modified: Wed, 11 Oct 2023 07:45:51 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
