## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:08be43346ec6128c0a6b105ae3a3769e782bad8c3fcd7563a93935fdbd873ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:9430f003520d46a71de6e114de7a9b34dd55ff737d8bff440a9b6dffa388f458
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394430751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a58dfcbe46b0f9389c30e47f9fee72eae019ebabb379e0a1ae39c794640c3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 20:00:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 20:00:47 GMT
ENV MONGO_VERSION=5.0.24
# Wed, 14 Feb 2024 20:00:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.24-signed.msi
# Wed, 14 Feb 2024 20:00:49 GMT
ENV MONGO_DOWNLOAD_SHA256=a83af50b58ce226c14235466ca5f88c4d5c40002cb8470118b5c8c42a6a27dac
# Wed, 14 Feb 2024 20:02:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:02:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Feb 2024 20:02:09 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 20:02:10 GMT
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
	-	`sha256:221fd5943321c7410203a10402536202c1dbe513e1353f303c2dc180543e2b07`  
		Last Modified: Wed, 14 Feb 2024 20:02:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6efd9cd672bda5fd0d6e4900907bfe9aafcacfcfe4f7e5d912f160a997590c`  
		Last Modified: Wed, 14 Feb 2024 20:02:13 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce9c35e4093b63acb7d96d82126d4aea3a80923e043938059dff2b00b8b2ed4`  
		Last Modified: Wed, 14 Feb 2024 20:02:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3059f424b1d3976ad5b16608df17a6de5708ed93af7b623699feebd6724a9002`  
		Last Modified: Wed, 14 Feb 2024 20:02:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df39e171f2fde8299c3fae3837b09aab11499d1ead220a5d91a506e6161a5428`  
		Last Modified: Wed, 14 Feb 2024 20:02:45 GMT  
		Size: 314.0 MB (313972886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942fd38c2c8082d83f0d9c5075e23fa22855acfa154bb5e37e72f560f3323c80`  
		Last Modified: Wed, 14 Feb 2024 20:02:12 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5559e08edd6f919152ce81e4b9f111f166d1e6cf1b67fb2d0731fe3c2d6ab06`  
		Last Modified: Wed, 14 Feb 2024 20:02:12 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a163fd7e7da23c8a97d1ee6ea41ef964eb962fa147b2e0fd0e53af87ed840b`  
		Last Modified: Wed, 14 Feb 2024 20:02:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
