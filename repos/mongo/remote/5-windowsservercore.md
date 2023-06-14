## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:f4c19376a7164400dcaf253d7cae4df24a39f3de1a7a922a3eef79e968d8e2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:544667cf33bb3c03bc8fb0c6c09fda2ced267d860523045ad6a564a44328993f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1702133809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1717711e7efa9b942f6ee20730f5838dc5e1e14df9d34d942333fc65f77c9f9d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 19:16:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 19:32:51 GMT
ENV MONGO_VERSION=5.0.18
# Wed, 14 Jun 2023 19:32:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.18-signed.msi
# Wed, 14 Jun 2023 19:32:53 GMT
ENV MONGO_DOWNLOAD_SHA256=369e0cdc34c29290bfcc9d47569e1debad1b86010ea5e00aefd7c670717f434b
# Wed, 14 Jun 2023 19:34:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Jun 2023 19:34:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jun 2023 19:34:19 GMT
EXPOSE 27017
# Wed, 14 Jun 2023 19:34:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45a9c91ac9cf27bb12f7baad712822dbb1e41b172e97946a8d48287c1570eb5`  
		Last Modified: Wed, 14 Jun 2023 19:49:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b5bcaacdf54903e5710db0acd1e25d6bbab9a59bb678b2122c9d85d9e810c5`  
		Last Modified: Wed, 14 Jun 2023 20:03:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f16466a4373661cebb976f08cdc1b2944d08edb754119db1f72ac13bb99efa`  
		Last Modified: Wed, 14 Jun 2023 20:03:01 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e68735115a16b7826ebce5dffe4ca3f6ced026963f7c74605f17250765c70`  
		Last Modified: Wed, 14 Jun 2023 20:02:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc986995e9d14158bbc15d551cbc634d8ce69ee629e95fa49d5b28e5efeaeb35`  
		Last Modified: Wed, 14 Jun 2023 20:03:56 GMT  
		Size: 313.5 MB (313525734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd7872bdc2443df8f6667be8e850e9301cc9452feb7c34de50d4c14fabc6352`  
		Last Modified: Wed, 14 Jun 2023 20:02:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6714d8e41bfd227df226512e433525611da73a448c165f2b06f97bdcb949c9f6`  
		Last Modified: Wed, 14 Jun 2023 20:02:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a91b1fc538353a31c07c18899328eacdab7cf4bc59e7785c8efb632a8d6e1f`  
		Last Modified: Wed, 14 Jun 2023 20:02:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:d2dd72bda4b8aa9f1d7a97b96afbd87bb0fb4ad7d102ba318b5afed0427a0466
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1964195302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971bb611763ab9ff08260ec51c424bb8494c37962724b28b5f19573e1c8389bc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 19:34:34 GMT
ENV MONGO_VERSION=5.0.18
# Wed, 14 Jun 2023 19:34:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.18-signed.msi
# Wed, 14 Jun 2023 19:34:36 GMT
ENV MONGO_DOWNLOAD_SHA256=369e0cdc34c29290bfcc9d47569e1debad1b86010ea5e00aefd7c670717f434b
# Wed, 14 Jun 2023 19:36:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Jun 2023 19:36:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jun 2023 19:36:12 GMT
EXPOSE 27017
# Wed, 14 Jun 2023 19:36:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f429cbe0d5bb38c019b37707ce67c088cd07b197ec74ccd1d4221ddff3f00253`  
		Last Modified: Wed, 14 Jun 2023 20:04:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1312b835f8f4d4804f27d4d768b58fabeceb14ba4a2aec3f3edfad341e0af736`  
		Last Modified: Wed, 14 Jun 2023 20:04:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be44e8492936ad4afa282167bf7a0dfd691d9bdbbafb3fa04b00fde7a37c7da`  
		Last Modified: Wed, 14 Jun 2023 20:04:08 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f125403a0f0edba137e70bfa61283cd0e4feb3469309e9fdddbafd7ab5d3a04`  
		Last Modified: Wed, 14 Jun 2023 20:05:04 GMT  
		Size: 313.6 MB (313565472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86787493aab5e7d03132ac1c593c8b399fd5282820e710dd3321a7d6f8ab47a7`  
		Last Modified: Wed, 14 Jun 2023 20:04:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5c39a057dc97179a6b3ea80499ea68755a8a411b48553186bb3960008fa46e`  
		Last Modified: Wed, 14 Jun 2023 20:04:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e656b82c528ee029c6474bd0d8b73e5ada36c2f38fcaf331aad62a4079e3632c`  
		Last Modified: Wed, 14 Jun 2023 20:04:08 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
