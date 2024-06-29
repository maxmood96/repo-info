## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:c73efbc946d88206b80770df1cf985636d28b0db45c90f2e006fb5b2e8133714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:77092b64be37f3b0b2892a11c4e70281578a829c79172dc497a1f12eca1528ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726989821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9107bad946e6707f68e19347432e7f9a3f34ba715d2bca77ea11720cb9b7a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Fri, 28 Jun 2024 23:55:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 28 Jun 2024 23:55:24 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 23:55:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Fri, 28 Jun 2024 23:55:25 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Fri, 28 Jun 2024 23:57:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 28 Jun 2024 23:57:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 28 Jun 2024 23:57:58 GMT
EXPOSE 27017
# Fri, 28 Jun 2024 23:57:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd61208c16770e7b6f1086224d285df9a3d1bab3aed447de9e1841323d15fcf5`  
		Last Modified: Fri, 28 Jun 2024 23:58:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031a00c2645e9ff89d47241865b6b7778dc668b8e624e4c744000f5e0576190b`  
		Last Modified: Fri, 28 Jun 2024 23:58:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459ea13c8c965953637da85b0925c1b54941e60c3a6c859734e26351a1f7add`  
		Last Modified: Fri, 28 Jun 2024 23:58:02 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8306ad4975d367ff5d8cf1a2428fe9f3319e2d461aa7f12cd5aeccc35b6136c3`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e99d8e789fede49ecf83c637d8065a9037f74d9286add5b654e658c41fe8c0c`  
		Last Modified: Fri, 28 Jun 2024 23:58:47 GMT  
		Size: 608.8 MB (608790545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a143d11fa7ed8bb9e89c28e4cdbc0064e5e69388ecaf8c5be628163e0718aca8`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addc4658fc847cc75ef5ac76127b69d9c54c86a97d93c97f12fcca2cbc163a44`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf82acf494a704f558c328bd607ea32faebbfd89079c2c4f117c58d11b7539e`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:dd85cab6304c859a1f3cf4abfb6db529eb5673074fa2a9c4d139495fa21f5bc4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2829632641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4159ebc29a28c284d8cdbdccb1ab50c906be9868de42c920de637960d2064e92`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 28 Jun 2024 23:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 28 Jun 2024 23:55:17 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 23:55:17 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Fri, 28 Jun 2024 23:55:18 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Fri, 28 Jun 2024 23:58:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 28 Jun 2024 23:58:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 28 Jun 2024 23:58:27 GMT
EXPOSE 27017
# Fri, 28 Jun 2024 23:58:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92aacc9f51ed7a59d66a611cef7bda8617d7cc761d89ab1e9c89b410c61a92`  
		Last Modified: Fri, 28 Jun 2024 23:58:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63f9f1cbd84670e9caf6a387e356fe324c705b811e2e390623904d66dd7b594`  
		Last Modified: Fri, 28 Jun 2024 23:58:31 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994df02ea50779784cbd775a9b5fbeff1732c4c9bea436bac2210057f1dd96f5`  
		Last Modified: Fri, 28 Jun 2024 23:58:32 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e402124f634bc0554258042bfc8a65d71901bdc716376522f51deca8c47b12c4`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5365be088357d7a26961dee5e3b86fe62af0a3ba6ff68a30d8bbfb04bcb450ac`  
		Last Modified: Fri, 28 Jun 2024 23:59:17 GMT  
		Size: 608.9 MB (608942369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcf702b18dc66be12ef3d759932934431590cb15b91cb978aafda1827ea8df3`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e85609069fc0d27983ce8cd12c3df256bc516272aa90c225abbb93d5382bd8`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41328de76efdf9a8bcec7cf8e6004eb1ed8c5fd90d15eb388e1210a89f89add`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
