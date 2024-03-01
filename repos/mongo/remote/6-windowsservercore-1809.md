## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c73cf843000deade8663d12462022d0cedb9d7244ca70a39f39edc24427e4aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:300a4adaec8e274fa4e8055af9a9f28abb16a2a98d2b5ae3947f67dc0f2e5ebe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2602565911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2e237c23bf9780b9b6722e15b207a5b5b6140726cbd3288b95b4e279bdd612`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 01 Mar 2024 00:49:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 01 Mar 2024 00:49:41 GMT
ENV MONGO_VERSION=6.0.14
# Fri, 01 Mar 2024 00:49:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.14-signed.msi
# Fri, 01 Mar 2024 00:49:42 GMT
ENV MONGO_DOWNLOAD_SHA256=871a352e6eb31f2d4d74816b6511cc350697c2004580f79f652f1a9237ea15c8
# Fri, 01 Mar 2024 00:52:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 01 Mar 2024 00:52:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 00:52:59 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 00:53:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778c3b1c7de283547305a08e71c9d2aa5f3059c2170aba4057dcc35d902a2347`  
		Last Modified: Fri, 01 Mar 2024 00:53:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb3fae798c188e86c986e53daaf9fabab60240faedc2733d0c2a624e43af11a`  
		Last Modified: Fri, 01 Mar 2024 00:53:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3dfd58eb65875aa823c974b4500e767f70e6fe05caad84fa4c1c6b544baddb`  
		Last Modified: Fri, 01 Mar 2024 00:53:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eb2b507aa62456b3b16f374569059534396f888efcabbe01e9d8be7988090d`  
		Last Modified: Fri, 01 Mar 2024 00:53:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67ce5c46de7329d974d060f80564824c2b267fd6dd09a7f0def021376772185`  
		Last Modified: Fri, 01 Mar 2024 00:53:48 GMT  
		Size: 522.1 MB (522108110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebf3cb85839e0e7068928fec24914c0b43dc8f2131d0cfa65d1d89f9420756b`  
		Last Modified: Fri, 01 Mar 2024 00:53:05 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c944d5ff9d5b0ac23e49972af7b13cdbe93cd778606b3fbf8a8e5db1df2c52`  
		Last Modified: Fri, 01 Mar 2024 00:53:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bbfb69e13c0176f9a2de13da80b837a6b74e8210928a71d3bf10f55ceba7c6e`  
		Last Modified: Fri, 01 Mar 2024 00:53:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
