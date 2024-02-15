## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:357b4b2220d20cfc5292f60c07bc297a1a1395c9855beba513aa4cea768f348a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull mongo@sha256:5a2e03e27784794bd71009c0095b33633ac09f0fb47a512eecfd7166bd084fb4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224607043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c41f4567f107fd5fd9d3abbcfb4bf759274c5d916df627d197ac87f699ced`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:02:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 20:02:19 GMT
ENV MONGO_VERSION=5.0.24
# Wed, 14 Feb 2024 20:02:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.24-signed.msi
# Wed, 14 Feb 2024 20:02:21 GMT
ENV MONGO_DOWNLOAD_SHA256=a83af50b58ce226c14235466ca5f88c4d5c40002cb8470118b5c8c42a6a27dac
# Wed, 14 Feb 2024 20:03:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:03:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Feb 2024 20:03:25 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 20:03:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2368db7e2c20d9b4a5c34d4017c1f5f1b50e589e2f643208438e8ad4b8088b6`  
		Last Modified: Wed, 14 Feb 2024 20:03:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2a8259d7c9447be6a4845bd1d640caf3f9807b683f101e5718e4fa07fdfaad`  
		Last Modified: Wed, 14 Feb 2024 20:03:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac68fbbcd66c6085de752080011ac7eaf2646762df1146a4f85ccf63a76bde71`  
		Last Modified: Wed, 14 Feb 2024 20:03:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c02c00b0d0c0c237440d43126ec89ec9375e9c9c2adebf36efb64928a7596b`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcd73137a74dee3c9f4eb83f1526b132112c46ae8f0e1489e75df1a2362473c`  
		Last Modified: Wed, 14 Feb 2024 20:04:03 GMT  
		Size: 313.9 MB (313943833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12997cc3871560d361e6e6eb3a5521c05d66c5ee554c1d60f7d44248cf79fa14`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5974a7ce3dcde7f1a786598bec76c0099c852e239cb45fb966c1e9279a5592`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43fd4ba32e8e8f034df928e11fe22879dc5e6b4fa64ff23c2019a53279a5028`  
		Last Modified: Wed, 14 Feb 2024 20:03:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.5458; amd64

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
