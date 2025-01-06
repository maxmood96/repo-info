## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:90b8b9111578559c4ae6789c9a6e364287c86208847d643e6f54635edb798033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:d5fe53b9faf12746f57e47167faa8e1c37823616d9e2a441c9530db748c598c4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2865634027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a059a00fff738837879379ad17153f6d1a329b63f37e876794ff2f49d0f74a2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Mon, 23 Dec 2024 17:27:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 23 Dec 2024 17:27:43 GMT
ENV MONGO_VERSION=7.0.16
# Mon, 23 Dec 2024 17:27:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.16-signed.msi
# Mon, 23 Dec 2024 17:27:44 GMT
ENV MONGO_DOWNLOAD_SHA256=88fe05d7f324e72b9d17cbfe9bde652053c398efc7cffc0249c944faf4f32b34
# Mon, 23 Dec 2024 17:30:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 23 Dec 2024 17:30:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 23 Dec 2024 17:30:23 GMT
EXPOSE 27017
# Mon, 23 Dec 2024 17:30:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1d7e65d96b6638672cf07f3a07c119b2efd6dd34a8d01ba35e7d63cd6c1df`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fef28e4ab8f0cb90cd370b7279d3919ace86e1fe21a584f1a079449753282b`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b182e6e4389b56d871ac1687f499adebd8fd7dd8d37c7872d579bb50b5286503`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0e9d2426eae6a40c0b4ec7df769e3f52edc9f68deba65f72cd361c1d4ba124`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8af615d46722608e49bee919f92cb932d056706845020c6a18acbc1b981ae8`  
		Last Modified: Mon, 23 Dec 2024 17:31:13 GMT  
		Size: 611.8 MB (611751404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4779750d2710a72199c613af9ed0021651dd50faf2cbb986deebd6e969d6a77`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cefd40f2fcdcdf84a5c15d3853d074ac48301beb7fdf5f30cf1cf6bb50c90e`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cffe5a7ddcfb7546bdce9ff76ca8eac0bd8c66b08c93d830b0e98858d870f34`  
		Last Modified: Mon, 23 Dec 2024 17:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:da09510a831b6c45e4267c6f37293d8a00faf04dc136b422f1dcf8e0fb45e3ad
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2626084994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9808d80770a60d4dbc155a64e3bff465b5f18dcbff6dc8977947ac7b2e80d5d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 23 Dec 2024 17:27:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 23 Dec 2024 17:27:39 GMT
ENV MONGO_VERSION=7.0.16
# Mon, 23 Dec 2024 17:27:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.16-signed.msi
# Mon, 23 Dec 2024 17:27:40 GMT
ENV MONGO_DOWNLOAD_SHA256=88fe05d7f324e72b9d17cbfe9bde652053c398efc7cffc0249c944faf4f32b34
# Mon, 23 Dec 2024 17:29:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 23 Dec 2024 17:29:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 23 Dec 2024 17:29:25 GMT
EXPOSE 27017
# Mon, 23 Dec 2024 17:29:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1b3e6c0adddfbdc49a1c76d483e59a2464670eb1cdbabdf1e9d4c5f36ed4fe`  
		Last Modified: Mon, 23 Dec 2024 17:29:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69c2afb3d50e6d30e29563047141c97a4ac73d90bd5e7ce6c423e2c3b37977d`  
		Last Modified: Mon, 23 Dec 2024 17:29:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06566f0b4d511cbd529852f26dd5b16df6bc216fde71b7ab2c55a4492ff970b`  
		Last Modified: Mon, 23 Dec 2024 17:29:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02995b54d573fe4559e2b3f201b780fd262501d1ba47b14e57aea80d7e23c77`  
		Last Modified: Mon, 23 Dec 2024 17:29:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c47c491e2f8cb55931de8bc8a3bc2f3362531b3f765f85d4969be27e0e74dcf`  
		Size: 611.9 MB (611905787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1e04b2a0539c75456068ca9a9cdc9ea17006e3adaebe1dc6245c97404e7cd2`  
		Last Modified: Mon, 23 Dec 2024 17:29:30 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efa3a7a03e6d6ffd1967ca2bb9e493386e96b0aef64af8f1f0b878b3d08ccca`  
		Last Modified: Mon, 23 Dec 2024 17:29:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b4b69775a17e6a1a319e1dd1057d3735f0c0c41f8a49a9aec6d5ae41e34221`  
		Last Modified: Mon, 23 Dec 2024 17:29:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
