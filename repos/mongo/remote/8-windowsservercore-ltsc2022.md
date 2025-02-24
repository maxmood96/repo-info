## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:60a836f2e06a0d30c9957c5d75e237bec0c4f41dde915bf39cd5f8531939795d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:ac1f75e90aa981f7c05b62783d6b8fe281faaf950b8621ff84d9d97803808e22
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3034851783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb92b7fddceb4425fd294cf9a989f1441e384c9f7d967d989a06b8facbf266e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Mon, 24 Feb 2025 21:38:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Feb 2025 21:38:38 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 21:38:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Mon, 24 Feb 2025 21:38:39 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Mon, 24 Feb 2025 21:40:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Feb 2025 21:40:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 21:40:04 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 21:40:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed1955a54a0ada7d85bb224eaed23cd71f69440b545ca678531da009ebdfe29`  
		Last Modified: Mon, 24 Feb 2025 21:40:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ab84b8249961b603325cd527d684cdd7cbdb13e83af81f5e5cb706a751072`  
		Last Modified: Mon, 24 Feb 2025 21:40:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0819825956ea690559527900402c65eb93f6dd246f97846a921cff69083a37`  
		Last Modified: Mon, 24 Feb 2025 21:40:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f47f19a7c43b9648e31ddb529c646dce1525b5cde13be7c6c358df027631c`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b003af40a6c1a7d520f85690d04d29b7cb394d58b9d002784df77c7470ade03`  
		Last Modified: Mon, 24 Feb 2025 21:41:11 GMT  
		Size: 771.0 MB (770984775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c635ad6951ee996a89ac6826edc17b154455a9813d9f2da44442943c0241a6c8`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e78fd5b0ff882752dc87c43e803bb8ce3ecc4604ad03b8c9125d9c476ff372`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426b8bb15e7e59c9e5bcdca0d41d0deedf29dd5e1e39b23e26e4422262ffa02`  
		Last Modified: Mon, 24 Feb 2025 21:40:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
