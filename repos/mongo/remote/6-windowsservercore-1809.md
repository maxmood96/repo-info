## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:5245f1a519c2730ba4a2e4238b80fda33d840bdc564da40f74815c782c26f581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:654bc32f636c5f7a4c41d6f76bc4a6edf35564d13f771468e709ddca0c9dbea0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549838346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6340b88feba178ae1723e7b7489bbe6f26ca2c9fb15943e6d43e1a38a67dcb30`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 13 Oct 2023 00:19:42 GMT
ENV MONGO_VERSION=6.0.11
# Fri, 13 Oct 2023 00:19:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.11-signed.msi
# Fri, 13 Oct 2023 00:19:43 GMT
ENV MONGO_DOWNLOAD_SHA256=178b163aa3a663766a792cce4eec0ca2624392bd82eb1274b91aa00f6345c34a
# Fri, 13 Oct 2023 00:22:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 13 Oct 2023 00:22:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 13 Oct 2023 00:22:28 GMT
EXPOSE 27017
# Fri, 13 Oct 2023 00:22:29 GMT
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
	-	`sha256:a3035a184e9ef2bd9826bf17afea11eebcc052e900074de41ed755270ece7e36`  
		Last Modified: Fri, 13 Oct 2023 00:28:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea9680c20189a4779b5e8ef796eb7ceb4a75d48ffd800945054514a9222cbbe`  
		Last Modified: Fri, 13 Oct 2023 00:28:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719331e21f225d24d7df5fe1ece68b2b72c056569a48e91625018ba63097a61b`  
		Last Modified: Fri, 13 Oct 2023 00:28:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23485a715c5b0ffaf5acde0a087cfc5714f23c3a4d3e7df86eb1ec7b8400e586`  
		Last Modified: Fri, 13 Oct 2023 00:29:24 GMT  
		Size: 518.2 MB (518238294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6681cf46e10b2c5c3e28ef3a8d1f063f9dda0406d3c67af424683a50f51dddd`  
		Last Modified: Fri, 13 Oct 2023 00:28:14 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab0ad8052330a7d7c3f94d0e5527e5c8b5b12412748eaea1ce498f16f0c6e46`  
		Last Modified: Fri, 13 Oct 2023 00:28:14 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d976a40b339eaebf341ab592ad2d28a2c9048cc6535dba1b97c24fc79d6347`  
		Last Modified: Fri, 13 Oct 2023 00:28:14 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
