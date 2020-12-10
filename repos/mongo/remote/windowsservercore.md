## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:42ba35f503318b3039408f01e76309c3b952929f4b6dbacfe093efa933ca0de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `mongo:windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull mongo@sha256:c413de7dceca5099916d534d77ea45f58533d417655882c70fdb5c7a81ca8893
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2630600330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bd142ab75b6f1db5fac44eb534c2deb5bb996e2375f7d8e410cb5c3428ec27`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 23:34:41 GMT
ENV MONGO_VERSION=4.4.2
# Wed, 09 Dec 2020 23:34:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.2-signed.msi
# Wed, 09 Dec 2020 23:34:43 GMT
ENV MONGO_DOWNLOAD_SHA256=84a1f6899e25f90a7d7c2b5996e9e15584a9af54c08832682c962c5794fcab0f
# Wed, 09 Dec 2020 23:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=ServerNoService,Client,Router,MiscellaneousTools' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Dec 2020 23:38:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Dec 2020 23:38:05 GMT
EXPOSE 27017
# Wed, 09 Dec 2020 23:38:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a22f4f88a098a1b5fbe19f0d98614e8a11ddf4c264990dfb45eecbf3bd45f`  
		Last Modified: Wed, 09 Dec 2020 23:53:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93bcbb4951bf2fc3084e5553a4ff60ae0f7c37599a657dd17a042e1dfcf91a`  
		Last Modified: Wed, 09 Dec 2020 23:53:36 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9147a862855224ba2b06d54855315014baea19893afefcc45b867ab769b94b88`  
		Last Modified: Wed, 09 Dec 2020 23:53:34 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db0edf76767f579a89de2495ddcda9b7b8d99db5c5608e91f12e18b1abe86f`  
		Last Modified: Wed, 09 Dec 2020 23:54:24 GMT  
		Size: 239.7 MB (239717872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce4a444e7656734bb1098bd50a0a2af224e46a6e4aee336e64c80e7a0d7fdc1`  
		Last Modified: Wed, 09 Dec 2020 23:53:34 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f9d681ad0c28cc87536bd26e8174acae0966becbd1504a87ff5248e3a22cc6`  
		Last Modified: Wed, 09 Dec 2020 23:53:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57225c862b33e747fe1d975f80a420d8442cdae58894f5fe170f27acbb642fa`  
		Last Modified: Wed, 09 Dec 2020 23:53:34 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull mongo@sha256:843618472ebde6d2d1c2589a9e2e06a2a1c650842ae7e6cda7e7f9261e8fe872
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6009351108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69008fe45d754cad9afd624a7df920134ca19d31f1f15c609e1cfe4c133f9008`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 23:38:23 GMT
ENV MONGO_VERSION=4.4.2
# Wed, 09 Dec 2020 23:38:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.2-signed.msi
# Wed, 09 Dec 2020 23:38:25 GMT
ENV MONGO_DOWNLOAD_SHA256=84a1f6899e25f90a7d7c2b5996e9e15584a9af54c08832682c962c5794fcab0f
# Wed, 09 Dec 2020 23:42:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=ServerNoService,Client,Router,MiscellaneousTools' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Dec 2020 23:42:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Dec 2020 23:42:25 GMT
EXPOSE 27017
# Wed, 09 Dec 2020 23:42:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0835224d9d9854c81b9359117c1f5ce83e66e6da8df30d0923952545a057346f`  
		Last Modified: Wed, 09 Dec 2020 23:54:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a169f4b513ea7b8e8523844a81fe78019061c86dee85172dd94dde11bfaeb163`  
		Last Modified: Wed, 09 Dec 2020 23:54:45 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c490da0543306c0a882a89b870f39c4a23b834126800b5f52ccfe9b7396544f`  
		Last Modified: Wed, 09 Dec 2020 23:54:42 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69e3d5bd337cd616bce442296fc5f2a091aac1a6760d049d7d9ba61f8b9079e`  
		Last Modified: Wed, 09 Dec 2020 23:55:26 GMT  
		Size: 240.5 MB (240499089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ef74ca488c44f482657528ea1168847e7db8e51e089b0ab95546a1376034a3`  
		Last Modified: Wed, 09 Dec 2020 23:54:42 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0634a5dfc14ed483a7b62bbe5160c09b570a85aeced87608bbd3896091636f`  
		Last Modified: Wed, 09 Dec 2020 23:54:43 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f076cac847e3fbe47001f736cbbb67d25f6cef890b2467c4a7022551e57f014`  
		Last Modified: Wed, 09 Dec 2020 23:54:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
