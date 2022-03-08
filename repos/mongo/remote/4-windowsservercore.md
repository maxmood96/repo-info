## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:d146fdf4bb79777f306cee70ac1242ea1ba6b0de5c45642e58535eeaacc7185b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `mongo:4-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull mongo@sha256:c97f23311ba0cf6fa321c65db17ee1511f608f96e929484368c048b28393864e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2464171125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95a127bb03943facd672bfa7a7d56a5044af21e02f340a80a5ee679941c6edd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 20:08:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 08 Mar 2022 20:16:13 GMT
ENV MONGO_VERSION=4.4.13
# Tue, 08 Mar 2022 20:16:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.13-signed.msi
# Tue, 08 Mar 2022 20:16:15 GMT
ENV MONGO_DOWNLOAD_SHA256=0eb6e5c43c74a992301529515c52b7e326239cd12649fb6f91e807fcbbf06f39
# Tue, 08 Mar 2022 20:17:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 08 Mar 2022 20:17:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:17:45 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:17:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:100676d020cbb3f3df522078bdbd67f9bbdab3dee71a4ec647a43b6b2b1e0b8f`  
		Last Modified: Tue, 08 Mar 2022 20:37:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdd547ff65b905c1ade24922a398fafbd6254cfe1e1d388d684d5919d0d8c14`  
		Last Modified: Tue, 08 Mar 2022 20:47:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318d58991fcc915edbe018bdca9b534b894a397ed2277d9ceecf39e13ce4eb35`  
		Last Modified: Tue, 08 Mar 2022 20:47:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87619370023a287ade03493fbe6a86a49b9ae5bdc7feebf89c6bc412d1c31e08`  
		Last Modified: Tue, 08 Mar 2022 20:47:15 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05855c6d57d32a03c5a27a49c01fbfd7d53a654bf5b56896abce526521220b3`  
		Last Modified: Tue, 08 Mar 2022 20:48:01 GMT  
		Size: 242.9 MB (242914859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe884ee584a047a66726f95bc7eeb47737def95215298e6e263c789cdcbaa594`  
		Last Modified: Tue, 08 Mar 2022 20:47:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1621fd9a787713795c7832727a9486fb8a2ec80ec67ed22fa963166e4a512b1`  
		Last Modified: Tue, 08 Mar 2022 20:47:15 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd077edb062479d8f7bc67c2b1327681db87516f9924a1d2d15b64c79939b3b0`  
		Last Modified: Tue, 08 Mar 2022 20:47:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull mongo@sha256:512e310e886ba97a31798d6a8334a35605227bd04fa39650d44bbaa83a13aed7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2958158870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65db7016384d46c6953c1812d563c07825f88db20f4ec90ca1e34d5b89d6724`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 08 Mar 2022 20:17:56 GMT
ENV MONGO_VERSION=4.4.13
# Tue, 08 Mar 2022 20:17:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.13-signed.msi
# Tue, 08 Mar 2022 20:17:58 GMT
ENV MONGO_DOWNLOAD_SHA256=0eb6e5c43c74a992301529515c52b7e326239cd12649fb6f91e807fcbbf06f39
# Tue, 08 Mar 2022 20:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 08 Mar 2022 20:20:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Mar 2022 20:20:10 GMT
EXPOSE 27017
# Tue, 08 Mar 2022 20:20:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655a37b3382b82c4c43d7dd4cafe10649430943b12c4501c705571a039fc998`  
		Last Modified: Tue, 08 Mar 2022 20:48:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a52eec6e8fef1133eafa096705f1303efc7ab241ffb2846cd2a8b5e475b954`  
		Last Modified: Tue, 08 Mar 2022 20:48:17 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8642db41c1f3bb720e81fd936c0914659b8fc0f34aa3039563ef523dedb9d2c`  
		Last Modified: Tue, 08 Mar 2022 20:48:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c9c966d3898b14f9e85b294a3addcace46cae7b87ba60d487d10a9a7d987a5`  
		Last Modified: Tue, 08 Mar 2022 20:53:01 GMT  
		Size: 242.7 MB (242696637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254b59a49423753ca43ccfab8eb4d4a73fcf68053e77c38d06f31b42efe178c`  
		Last Modified: Tue, 08 Mar 2022 20:48:14 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e300ce4c77068c3e07a1116911d344f43c05c67fccd6afec9ced6bfb2c28481`  
		Last Modified: Tue, 08 Mar 2022 20:48:14 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ae0506a8f94052501563b9c534dbe355a0385ccf0d793f1b12508eba5e61f`  
		Last Modified: Tue, 08 Mar 2022 20:48:14 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
