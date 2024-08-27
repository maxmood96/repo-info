## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:ed2a77e98784ce93b419df71c00d6b01e88046c78e0c685c51c6a9048fee78a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:b11f4e7fa642dba9418544a3f9d392fec257eb5b4322059164e288d2850d99d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2854921419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cb306282371ae1c22c6cd735a55bd9e8ca329b11b9318f9a5e867236b0fda4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 26 Aug 2024 22:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 26 Aug 2024 22:55:47 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 22:55:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Mon, 26 Aug 2024 22:55:49 GMT
ENV MONGO_DOWNLOAD_SHA256=8916397b35f2b6b42241ef1625e5c75ba7ad10ad75072cf377450f6f0bdf254c
# Mon, 26 Aug 2024 22:58:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 26 Aug 2024 22:58:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 26 Aug 2024 22:58:41 GMT
EXPOSE 27017
# Mon, 26 Aug 2024 22:58:42 GMT
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
	-	`sha256:426ba3cbf779c29063646390e2920f16d65c396af1f72f2dc4e5b4d811ad8177`  
		Last Modified: Mon, 26 Aug 2024 22:58:45 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85581ed0a705e2953dc01caf000485162ac3ff208f1482ce32f135436b25f465`  
		Last Modified: Mon, 26 Aug 2024 22:58:45 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597e761832c450162e922f32808f815ce2ec986f7dd7bc2e726cc6f32e73223d`  
		Last Modified: Mon, 26 Aug 2024 22:58:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213755ad8daacaba8b937bd2b7873bb5da7d29c8745c25da8c92fdda0f8c4c0a`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd73cb761835860fd24006bb0554e3e4cd440c468e7c48adc258c972f95599d`  
		Last Modified: Mon, 26 Aug 2024 22:59:30 GMT  
		Size: 609.7 MB (609709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae5832247bf9fb4cb0f646d14538c266b3ad7dd05f5cf1a371884ca2169dc44`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820397eeedc6daf8ec59dc3751c65c21b0e054241e4e5f091ef015988456288e`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e114ad3497cbe1f1556a043aa7ce451911deb4b6ce2c149342919638f9976fab`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
