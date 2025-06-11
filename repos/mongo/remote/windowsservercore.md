## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:7752cd8b29b88cd4e8eed256b4f1a7cf27c7e1314ae81a594a1eb81cffc06616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull mongo@sha256:eafc704b169af6ef05eb9310626a4806fe2d49ba4ef94745ead87d3f1cece488
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4251469207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f9cc2cac06ada1ba93fddffaafbdc692d1f358bcf1db2afa84c4064a90d7f9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:28:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:28:39 GMT
ENV MONGO_VERSION=8.0.10
# Tue, 10 Jun 2025 21:28:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.10-signed.msi
# Tue, 10 Jun 2025 21:28:42 GMT
ENV MONGO_DOWNLOAD_SHA256=ae5f02f81ba456ee9fcf819c362255ccae9a961f039435a09b6887f46732c940
# Tue, 10 Jun 2025 21:30:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:30:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Jun 2025 21:30:25 GMT
EXPOSE 27017
# Tue, 10 Jun 2025 21:30:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb62f4db31c85b2c5c3bcf8d8e1ca71f09966640602e23e6972472902f02371`  
		Last Modified: Tue, 10 Jun 2025 21:34:25 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12572d67d20fa4e2e73f061263b2b7aee3442ce020964c812bc91a17be4483`  
		Last Modified: Tue, 10 Jun 2025 21:34:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f636b2f99e9a0ae9ef253fedd9922ce78ad98107710a8bba4d4a4a1f8bdda97d`  
		Last Modified: Tue, 10 Jun 2025 21:34:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bfa73f768b1ca3301cb7f771313602f459128f962257f720a960332ce78ac2`  
		Last Modified: Tue, 10 Jun 2025 21:34:25 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f16b5fd28dd1a661b7525d2953d3c38cefce4db8a4da392b33302755191002`  
		Last Modified: Wed, 11 Jun 2025 01:09:07 GMT  
		Size: 775.3 MB (775286117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d72abdc08dd4eb5efa83660784d46b359c08338d205017e4f2f71f0d0ae6d2`  
		Last Modified: Tue, 10 Jun 2025 21:34:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702234c362874784cb3ce9b249470a49c22cef39af2821c7935359b6499549c`  
		Last Modified: Tue, 10 Jun 2025 21:34:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b1a1fa5666f27f9d7406c163a200f124c28117005e2bfb60dbaaab5bf0a1dc`  
		Last Modified: Tue, 10 Jun 2025 21:34:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull mongo@sha256:bab61028b9138688ab10f60d7a97f7ae593f1166afbf61f1757877681173111d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3055530116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c27b5b99ec10cdc6698615cf7adc2af4479896dab9fe214e404d0dbc2e53bf2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:26:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:26:03 GMT
ENV MONGO_VERSION=8.0.10
# Tue, 10 Jun 2025 21:26:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.10-signed.msi
# Tue, 10 Jun 2025 21:26:05 GMT
ENV MONGO_DOWNLOAD_SHA256=ae5f02f81ba456ee9fcf819c362255ccae9a961f039435a09b6887f46732c940
# Tue, 10 Jun 2025 21:27:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:27:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Jun 2025 21:27:36 GMT
EXPOSE 27017
# Tue, 10 Jun 2025 21:27:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee01c7b0c4b12e40af7644c0d32373eaa10e5087c02545fa5c8924aef6fdffb4`  
		Last Modified: Tue, 10 Jun 2025 22:09:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b941dd59fcd8e5673d42319466f804c80352a10811aee45d2b553cfb98e2e95f`  
		Last Modified: Tue, 10 Jun 2025 22:09:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5f2d737890d7350b5979699f3ca034c7d5b722855dbe0e4813eae9f6a0c46a`  
		Last Modified: Tue, 10 Jun 2025 22:09:23 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e36338bb739ffdf93168946db99399e81b31a18cfe600913613972c07461368`  
		Last Modified: Tue, 10 Jun 2025 22:09:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff5ebae3500cf0fd4cbac4354b72b4b351ef7dff6064a57f828696b28e76093`  
		Last Modified: Tue, 10 Jun 2025 22:09:34 GMT  
		Size: 775.3 MB (775269555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a21dde5bd2a2a73cd15d2a8178bb5ed5bed199cfaeb6469bbb68837d313c4ff`  
		Last Modified: Tue, 10 Jun 2025 22:09:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93cfafacf15055c801cb1ff470b4e46d919b5a8f2a2cf61691239db14d8cb31`  
		Last Modified: Tue, 10 Jun 2025 22:09:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f8d25940f7a8c8f2ea73286342cd9656a407e4e1f05a08f71417dab1a1596c`  
		Last Modified: Tue, 10 Jun 2025 22:09:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
