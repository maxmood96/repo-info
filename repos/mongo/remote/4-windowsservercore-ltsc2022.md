## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:e061bf6b494a90e5291c66164c1f44056762a428d46e9f60bfa8c465465ae0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.469; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.469; amd64

```console
$ docker pull mongo@sha256:1d1658398739bee863982cc04e722ae48d99495f1cc33cdee36ce5bed4d63cec
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442413731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1430a2f6ad1115534f978d5e0cef5bb8e5cb706643d6337a6a22b853edd8b6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 06 Jan 2022 03:56:33 GMT
RUN Install update ltsc2022-amd64
# Tue, 11 Jan 2022 19:59:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 20:01:26 GMT
ENV MONGO_VERSION=4.4.11
# Tue, 11 Jan 2022 20:01:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.11-signed.msi
# Tue, 11 Jan 2022 20:01:28 GMT
ENV MONGO_DOWNLOAD_SHA256=40b6f28996f80e4c1922c6e4b61cec0bc16f72cb2f35cb997e64a3a6b6f95074
# Wed, 12 Jan 2022 04:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jan 2022 04:12:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jan 2022 04:12:21 GMT
EXPOSE 27017
# Wed, 12 Jan 2022 04:12:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b593686e27e7562a5b0696823307ffa822214cee8bd2eec1075eadad4cb9712`  
		Size: 956.0 MB (956001983 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:304b58b2bd8a968bdbcff36b25fec940dbb658b60fa8fb3695b63e3e2a4cdcff`  
		Last Modified: Wed, 12 Jan 2022 17:11:29 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e872cf99cf8f67235f04db8c3bee6120941d3a9bdbdf3908706e0dfbcb4ea40e`  
		Last Modified: Wed, 12 Jan 2022 17:41:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250f378c4149e61499a1376d58a2eb5d34f302cf555cb50298bbb7236c3c5861`  
		Last Modified: Wed, 12 Jan 2022 17:41:58 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f337157a60391a9cab2333caf9fa60bb611ed0d9b4ba2c172ce8189f062a18`  
		Last Modified: Wed, 12 Jan 2022 17:41:56 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d83963ae171e5f367bbc727b3c9022567b8c1f276a50e1e9678f5e6ea74047`  
		Last Modified: Wed, 12 Jan 2022 17:42:43 GMT  
		Size: 234.7 MB (234702747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1435f4bec1c69d8e5e46d4ec90177ce9c18437bef8d5451e4893a46f8c36ae`  
		Last Modified: Wed, 12 Jan 2022 17:41:56 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c1de503801e8cf496d424e4c115356793f236d900233696b4a0b72254ebb8`  
		Last Modified: Wed, 12 Jan 2022 17:41:56 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91c707448e2a45ec6d72523fb471df3d52512c7a8b8b38ec03af0fe311b903d`  
		Last Modified: Wed, 12 Jan 2022 17:41:56 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
