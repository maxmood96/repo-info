## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:b6a36e4b72d2e52ab1f8c6ea2372b5ea1dc1d1ac597dfa12d575fd887d3147e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:4816a99d607799658e905299a7b8a8da82419e9c9a298cc40eb00b9e09b9ded1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2214445933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9febf47eab266fd995e5e84782c466ee202d6487feb1ebcd2dcf7dd2e936fcc2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:08:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:08:42 GMT
ENV MONGO_VERSION=5.0.29
# Wed, 09 Oct 2024 23:08:43 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.29-signed.msi
# Wed, 09 Oct 2024 23:08:46 GMT
ENV MONGO_DOWNLOAD_SHA256=3188d1a49244ce4a6bc4d853a3d79c178a9d0ae5e6613e4f42cf4156e6b25178
# Wed, 09 Oct 2024 23:10:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:10:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:10:42 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:10:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21daf2809f524efdc921e545e31decd36d2bb68883b6ed6fcd78fab222c4087`  
		Last Modified: Wed, 09 Oct 2024 23:10:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea456414357f44ca8b59c5b49d95b558fabef0522ec01db0156e67cbcafccc9`  
		Last Modified: Wed, 09 Oct 2024 23:10:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4450637076863ff8c05e5a467775898a7ecb9350f21f10dafcddee7da5518491`  
		Last Modified: Wed, 09 Oct 2024 23:10:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdab74e31d4c9e2e6487fce84b0a311ce3f4f8b50060c9218dfb45240da938f0`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3633041e16644f30c31b80fb46abfef5c26bc732cfd3d6bc0705f02231dfd5`  
		Last Modified: Wed, 09 Oct 2024 23:11:16 GMT  
		Size: 312.6 MB (312611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb78a7fbb6f645d1a084627f1953f9196b424b3c547b0f8caf3f014f6fe037`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc9a40eb0407009e53f6355e9c70700ac2406bd59c81eb37bb848509621838f`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8324e1648d176c09105410759ecb392580b842643eeea8b4d05f4856e16a2ea0`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
