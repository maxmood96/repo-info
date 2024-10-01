## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:25c04ec5bf85b60ddb0599023cc1ce494068e713302801865a6a7739be05c594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:148132fd67be8d370f7ba98460462b140f8c82d91a6cdab9c8caab14cabe8e39
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2244997485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ab17378db8392e6f8f02327b938d9a3a0d19e9845e24350d075b658d19f3a4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 01 Oct 2024 01:02:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 01 Oct 2024 01:03:04 GMT
ENV MONGO_VERSION=6.0.18
# Tue, 01 Oct 2024 01:03:05 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.18-signed.msi
# Tue, 01 Oct 2024 01:03:07 GMT
ENV MONGO_DOWNLOAD_SHA256=5aa85635f0b1f2f4e0a1d22410d507c8f4f1d9de0fa640fea1bcb5d8e4a6dee5
# Tue, 01 Oct 2024 01:05:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 01 Oct 2024 01:05:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Oct 2024 01:05:18 GMT
EXPOSE 27017
# Tue, 01 Oct 2024 01:05:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af906bb473b7d3f9e88a98de7628e4e8f961cd33232b4fe6ae4c910d6a7765d`  
		Last Modified: Tue, 01 Oct 2024 01:05:23 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d966b190ea3666471663e6af253fb0d70f0d024d954c5b480b5969506f11a`  
		Last Modified: Tue, 01 Oct 2024 01:05:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c080b58f5be924652d7917e82c0c372f59144445eb7bb8175d9b821932a4d`  
		Last Modified: Tue, 01 Oct 2024 01:05:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cae291cc5492996e8a514d746a80442838f5cbcec547f958d441231e771cbf1`  
		Last Modified: Tue, 01 Oct 2024 01:05:22 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c369cd6260bd2b226d0f1ba2635cedcfe36c6d69b4239bc8f21e20aec935b874`  
		Last Modified: Tue, 01 Oct 2024 01:06:02 GMT  
		Size: 524.7 MB (524720052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5974d18770f7a4feafce55ebf4fc749e1837a6cf320c6e67bb4165ef8f0d4d8b`  
		Last Modified: Tue, 01 Oct 2024 01:05:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5030f15a4710a7eaee928fd73d6eecbe97feda9e3eebc93b0f44d6b207e589cf`  
		Last Modified: Tue, 01 Oct 2024 01:05:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcc797d82fe41c687786db26286e67f11e885a61d96584ecc90269b979edd21`  
		Last Modified: Tue, 01 Oct 2024 01:05:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
