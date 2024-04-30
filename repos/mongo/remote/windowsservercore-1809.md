## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:e1ff87b4166ddcd24f97a0d06505b985ab6436fbd25e471b6a50ae6fd2e9124b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:83567b31934c42bfc04bd303846e62fcab650de1a034fbe3eda0e20682a4f02b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2782774828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6497364e418203ab2ccbff494aca7efd91178afa06b18f73da11b42110ac4fff`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Mon, 29 Apr 2024 23:50:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Apr 2024 23:50:04 GMT
ENV MONGO_VERSION=7.0.9
# Mon, 29 Apr 2024 23:50:05 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.9-signed.msi
# Mon, 29 Apr 2024 23:50:06 GMT
ENV MONGO_DOWNLOAD_SHA256=16be51285ed6042c39a8692b5cfed3413f53b37111f54861a72857af6e5cfa90
# Mon, 29 Apr 2024 23:54:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 29 Apr 2024 23:54:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 29 Apr 2024 23:54:15 GMT
EXPOSE 27017
# Mon, 29 Apr 2024 23:54:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2cf82bd1262bae36183fe08b8a7690679f1ff332bbcbff0edfd0ffc9b34a3`  
		Last Modified: Mon, 29 Apr 2024 23:54:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9535f9ae8b002a596482fdc03083b85a2163e9f5caa968361d836ba48868a61e`  
		Last Modified: Mon, 29 Apr 2024 23:54:19 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4a493142c788508546b93db625afeee8d24ec3493355ef1ba788bf48afae9`  
		Last Modified: Mon, 29 Apr 2024 23:54:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1c4f492e027ddb2393e849a968a155c1d963af69b7dad6cc6cca0d58b83d7a`  
		Last Modified: Mon, 29 Apr 2024 23:54:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f29a664d45ef6f91e9e9b93e4ace5e1914dd44ead79394ae85371e2debfecb`  
		Last Modified: Mon, 29 Apr 2024 23:55:06 GMT  
		Size: 618.3 MB (618337766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0011aa0b92efd5a92dc5befdf3c3a02f8fa40017d8f5eb1eee2701de7ca9a9`  
		Last Modified: Mon, 29 Apr 2024 23:54:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd59d7cf4682a2874bfa3f02c7bab07674122180b17936cfda0d2b40a76ea7a`  
		Last Modified: Mon, 29 Apr 2024 23:54:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faac06f2036f417c983e22f02698e767aa3b8cf7b622e28422d8c5137f724f9d`  
		Last Modified: Mon, 29 Apr 2024 23:54:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
