## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c8a0296a459a94edf9fa7fec6564977e5f947e83c87ffa4f85c1e99882202b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:0a3bbf66b1badad88133b1497513d189c66e112bb181b0cad60e55ebeb7b08c4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2589239893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a53017dffe336d5a78604b5ca83b95058e508d3b272d8298197df90293e4e2f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 18 Jan 2024 23:58:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 18 Jan 2024 23:58:27 GMT
ENV MONGO_VERSION=6.0.13
# Thu, 18 Jan 2024 23:58:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.13-signed.msi
# Thu, 18 Jan 2024 23:58:28 GMT
ENV MONGO_DOWNLOAD_SHA256=e47fa3e1ed73d1ea4fa4459efd2b36ee6d3b4c13b45403ce71db179aff53a7b4
# Fri, 19 Jan 2024 00:00:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 00:00:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:00:19 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:00:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed708a47c8a6884b5750d88dd9e8a064be46933c4bcfe01571f15027d8f09cb7`  
		Last Modified: Fri, 19 Jan 2024 00:00:26 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5c42809006bcfd66f37e0d9fe3fbc12a75d2854256d3811a1bf33671c5ae83`  
		Last Modified: Fri, 19 Jan 2024 00:00:26 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b486447ac3e4534612f0f08d7db64dee4295ff7929e8c53e010d638441a0afb7`  
		Last Modified: Fri, 19 Jan 2024 00:00:26 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4dc43cab94a98f7d72b599db27ef03b22e060a3db13806022b335a6d319d39`  
		Last Modified: Fri, 19 Jan 2024 00:00:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e869c2376927f3f73e7156e7b8566535473c94f7a6092f7ad763930a011c25`  
		Last Modified: Fri, 19 Jan 2024 00:01:06 GMT  
		Size: 519.5 MB (519507815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2d9218d9477d2559e2065d06e7e4c059210c9a56b0e74418f49f26a26a98e8`  
		Last Modified: Fri, 19 Jan 2024 00:00:24 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d537faff6f35fadea03291fb57f788f12d535af67456e9723de7ba8078a74004`  
		Last Modified: Fri, 19 Jan 2024 00:00:24 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e58d4bb91b554c8fda07bc18ae1e0633e95936c6b9f7dd85cf7cae8497499d`  
		Last Modified: Fri, 19 Jan 2024 00:00:24 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
